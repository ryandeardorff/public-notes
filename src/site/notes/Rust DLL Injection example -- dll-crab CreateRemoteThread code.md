---
{"dg-publish":true,"permalink":"/rust-dll-injection-example-dll-crab-create-remote-thread-code/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#cs #rust #modding 
> [[🌟 Me/Modding/DLL Injection|DLL Injection]]

This is a section of the source from: [dll-crab (github)](https://github.com/aiocat/dll-crab), in particular: [mod.rs from dll-crab (github)](https://github.com/aiocat/dll-crab/blob/67aa15583112c3fe2919ebc9803393c8318eff6f/src/injector/mod.rs)
```rust

// inject dll with CreateRemoteThread method
pub fn inject_create_remote_thread(pid: u32, dll_path: &str) -> bool {
    // c-compatible string for injecting to process memory
    let path_to_dll = wrapper::c_string(dll_path);
    if path_to_dll.is_none() {
        return false;
    }
    let path_to_dll = path_to_dll.unwrap(); // shadowing

    // get process
    let process = wrapper::open_process(pid);
    if process.is_none() {
        return false;
    }
    let process = process.unwrap(); // shadowing

    // alloc adress and write it for dll path
    let adress = wrapper::write(process, path_to_dll);
    if adress.is_none() {
        return false;
    }
    let adress = adress.unwrap(); // shadowing

    // get load library
    let load_library = wrapper::get_load_library();

    // load dll
    let mut thread_id = 0;
    let thread_process = unsafe {
        CreateRemoteThread(
            process,
            ptr::null_mut(),
            0,
            Some(mem::transmute(load_library)),
            adress,
            0,
            &mut thread_id,
        )
    };

    // check if dll loaded
    if thread_process.is_null() {
        wrapper::free_process(process, thread_process, adress);
        return false;
    }

    // check status and wait for thread and get thread exit code
    if !wrapper::check_process_thread(thread_process, adress) {
        return false;
    }

    wrapper::wait_for_thread(thread_process);

    if !wrapper::get_thread_exit_code(thread_process, adress) {
        return false;
    }

    // de-alloc memory, free libraries (memory safety)
    wrapper::free_process(process, thread_process, adress)
}
```