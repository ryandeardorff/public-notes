---
{"dg-publish":true,"permalink":"/rust-ffi-c-calling-convention-code-for-dlls-in-rust/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#cs #rust

### Declaring a function available in the dll..
```rust
#[no_mangle] 
pub extern "C" fn ...
```
`#[no_mangle]` prevents name mangling
`pub extern "C"` is straight up from c++ -- it defines the calling convention and restrictions.
[FFI - The Rustonomicon (rust-lang.org)](https://doc.rust-lang.org/nomicon/ffi.html#rust-side)
### Build
Then, to compile Rust code as a shared library that can be called from C, add the following to your `Cargo.toml`:

```
[lib] 
crate-type = ["cdylib"]
```

(NOTE: We could also use the `staticlib` crate type but it needs to tweak some linking flags.)
[FFI - The Rustonomicon (rust-lang.org)](https://doc.rust-lang.org/nomicon/ffi.html#rust-side)