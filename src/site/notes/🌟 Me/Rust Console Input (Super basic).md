---
{"dg-publish":true,"permalink":"/me/rust-console-input-super-basic/","dgHomeLink":true,"dgPassFrontmatter":false}
---

# Rust Console Input (Super basic)
#cs #rust

`std::io::stdin().read_line` with **output passed in by mutable reference** is super simple and part of the std library 👍
```rust
let _b1 = std::io::stdin().read_line(&mut line).unwrap();
```
the **return** type is the **number of bytes read**.