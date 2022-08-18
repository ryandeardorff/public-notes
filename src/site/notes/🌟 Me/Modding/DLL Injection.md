---
{"dg-publish":true,"permalink":"/me/modding/dll-injection/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#cs #modding 
> [[🌟 Me/Modding/Game Modding Hub|Game Modding Hub]]

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
If this value is TRUE, processes created by this process will inherit the handle. Otherwise, the processes do not inherit this handle. The [apriorit tutorial](https://www.apriorit.com/dev-blog/679-windows-dll-injection-for-api-hooks) sets this to `FALSE`. But I haven't done more research into why that is the case at the moment.

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