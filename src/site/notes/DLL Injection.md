---
{"dg-publish":true,"permalink":"/dll-injection/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#cs #modding 
> [[Game Modding Hub|Game Modding Hub]]

DLL injection is where you use a DLL to run code inside an existing process on windows by getting it within the same address space.

### DLL Injection with CreateRemoteThread
Resources:
* [DLL Injection Techniques (apriorit)](https://www.apriorit.com/dev-blog/679-windows-dll-injection-for-api-hooks)
* [CreateRemoteThread function (processthreadsapi.h) - Win32 apps | Microsoft Docs](https://docs.microsoft.com/en-us/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)
* [[Rust DLL Injection example -- dll-crab CreateRemoteThread code|Rust DLL Injection example -- dll-crab CreateRemoteThread code]]

CreateRemoteThread Signature (from the [docs](https://docs.microsoft.com/en-us/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)):
```cpp
HANDLE CreateRemoteThread(
  [in]  HANDLE                 hProcess,
  [in]  LPSECURITY_ATTRIBUTES  lpThreadAttributes,
  [in]  SIZE_T                 dwStackSize,
  [in]  LPTHREAD_START_ROUTINE lpStartAddress,
  [in]  LPVOID                 lpParameter,
  [in]  DWORD                  dwCreationFlags,
  [out] LPDWORD                lpThreadId
);
```
This is the function that will actually do the injecting. But in order to call it we will first need the parameters.

#### Getting a handle to an open process:
OpenProcess Signature ([docs](https://docs.microsoft.com/en-us/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)):
```cpp
HANDLE OpenProcess(
  [in] DWORD dwDesiredAccess,
  [in] BOOL  bInheritHandle,
  [in] DWORD dwProcessId
);
```
**`dwDesiredAccess`**
This will give us access to different levels of control over the process, *at the very least we'll want* `PROCESS_CREATE_THREAD` which will let us create the remote thread. But the other values are listed [here](https://docs.microsoft.com/en-us/windows/win32/procthread/process-security-and-access-rights). Useful ones include: `PROCESS_VM_READ`, `PROCESS_VM_WRITE`, and `PROCESS_VM_OPERATION`.

**`bInheritHandle`**
If this value is TRUE, processes created by this process will inherit the handle. Otherwise, the processes do not inherit this handle. The [apriorit tutorial](https://www.apriorit.com/dev-blog/679-windows-dll-injection-for-api-hooks) *sets this to `FALSE`*. But I haven't done more research into why that is the case at the moment.

**`dwProcessId`**
This is fairly self-explanatory, it's the *target process id*. But there's some more notes about this in the [docs](https://docs.microsoft.com/en-us/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) that apply to some other use-cases.

So an example of this might be ([source](https://www.apriorit.com/dev-blog/679-windows-dll-injection-for-api-hooks)):
```cpp
HANDLE processHandle = OpenProcess(
               PROCESS_CREATE_THREAD | // For CreateRemoteThread
               PROCESS_VM_OPERATION  | // For VirtualAllocEx/VirtualFreeEx
               PROCESS_VM_WRITE,       // For WriteProcessMemory
               FALSE,                  // Don't inherit handles
               processPid);            // PID of our target process
```

#### Write the DLL path into the target process memory
First we will need the number of bytes used to store the path. And from there we will use `VirtualAllocEx` to allocate the memory in the process. Then finally using `WriteProcessMemory` to fill that allocated memory with the DLL path.

VirtualAllocEx Signature ([docs](https://docs.microsoft.com/en-us/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex)):
```cpp
LPVOID VirtualAllocEx(
  [in]           HANDLE hProcess,
  [in, optional] LPVOID lpAddress,
  [in]           SIZE_T dwSize,
  [in]           DWORD  flAllocationType,
  [in]           DWORD  flProtect
);
```
**`hProcess`**
The process handle from before.

**`lpAddress`** 
Starting address for the region of pages you want to allocate. There's a bunch more details in the [docs](https://docs.microsoft.com/en-us/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) about this one, but for our purposes (at least as [apriorit](https://www.apriorit.com/dev-blog/679-windows-dll-injection-for-api-hooks) has it) *we can pass in `NULL`*. This is another parameter I haven't had the chance to dive crazy far into.

**`dwSize`**
This is the size of memory to allocate, in bytes. For our case that should be *the number of bytes used to store the path*.

**`flAllocationType`**
The type of memory allocation.
There's a ton of useful details and information in the [docs](https://docs.microsoft.com/en-us/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) on this one. But for our use case *`MEM_COMMIT` is fine*, which should attempt to commit the address range-- it guarantees that when the caller later initially accesses the memory, the contents will be zero. Actual physical pages are not allocated unless/until the virtual addresses are actually accessed.
-- To me that has read as, since this is virtual memory, the physical memory won't be reserved (as would happen with `MEM_RESERVE` or `MEM_COMMIT | MEM_RESERVE`) until the process actually tries to access that section of virtual memory, at which point it will be reserved in physical memory. Neat 😎

**`flProtect`**
Memory protection for the allocated region of pages. If they are being committed you can specify any one of the [protection constants](https://docs.microsoft.com/en-us/windows/win32/Memory/memory-protection-constants).
There's a bunch of these, which isn't all that surprising. We're just looking for something simple though, and *`PAGE_READWRITE` will do nicely*. It's read-only or read/write access to the committed region. (there's slightly more in the docs but it shouldn't matter for this use case)

So an example might be ([source](https://www.apriorit.com/dev-blog/679-windows-dll-injection-for-api-hooks)):
```cpp
// How many bytes we need to hold the whole DLL path
int bytesToAlloc = (1 + lstrlenW(injectLibraryPath)) * sizeof(WCHAR);
  
// Allocate memory in the remote process for the DLL path
LPWSTR remoteBufferForLibraryPath = LPWSTR(VirtualAllocEx(
        processHandle, NULL, bytesToAlloc, MEM_COMMIT, PAGE_READWRITE));
```

**Writing the memory:**
WriteProcessMemory Signature ([docs](https://docs.microsoft.com/en-us/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory))
```cpp
BOOL WriteProcessMemory(
  [in]  HANDLE  hProcess,
  [in]  LPVOID  lpBaseAddress,
  [in]  LPCVOID lpBuffer,
  [in]  SIZE_T  nSize,
  [out] SIZE_T  *lpNumberOfBytesWritten
);
```
**`hProcess`**
It's the *process handle*, you know the drill.

**`lpBaseAddress`**
Pointer to the base address in the specified process where the data will be written. There's some more details in the [docs](https://docs.microsoft.com/en-us/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) about how this can fail, but it's basically what you'd expect-- write access, sizes, and the like. We use *the result from VirtualAllocEx* in this case.

**`lpBuffer`**
Pointer to the buffer containing the data to be written. In our case, the path.

**`nSize`**
The number of bytes to be written. In our case, the size of the path in bytes-- same as what was used in VirtualAllocEx.

**`lpNumberOfBytesWritten`**
This is an *optional output*. *We'll pass in `NULL`* for this use case. But feel free to read the [docs](https://docs.microsoft.com/en-us/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) for more info-- it's about what you'd expect.

So an example might be ([source](https://www.apriorit.com/dev-blog/679-windows-dll-injection-for-api-hooks)):
```cpp
// Put the DLL path into the address space of the target process
WriteProcessMemory(processHandle, remoteBufferForLibraryPath,
            injectLibraryPath, bytesToAlloc, NULL);
```

#### Creating the new thread to load the DLL
We'll use [GetProcAddress](https://docs.microsoft.com/en-us/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) and [GetModuleHandleW](https://docs.microsoft.com/en-us/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlew) to get the real address of `LoadLibraryW` in `Kernel32.dll`

Like [so](https://www.apriorit.com/dev-blog/679-windows-dll-injection-for-api-hooks):
```cpp
PTHREAD_START_ROUTINE loadLibraryFunction = PTHREAD_START_ROUTINE>(
        GetProcAddress(GetModuleHandleW(L"Kernel32"), "LoadLibraryW"))
```

And then finally use [CreateRemoteThread](https://docs.microsoft.com/en-us/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) to call that `LoadLibraryW` we got earlier, like so: ([source](https://www.apriorit.com/dev-blog/679-windows-dll-injection-for-api-hooks))
```cpp
// Create remote thread that calls LoadLibraryW
HANDLE remoteThreadHandle = CreateRemoteThread(processHandle,
        NULL, 0, loadLibraryFunction, remoteBufferForLibraryPath, 0, NULL);
```