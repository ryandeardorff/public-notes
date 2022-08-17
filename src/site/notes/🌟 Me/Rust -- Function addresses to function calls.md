---
{"dg-publish":true,"permalink":"/me/rust-function-addresses-to-function-calls/","dgHomeLink":true,"dgPassFrontmatter":false}
---

#cs #rust #modding 
> [[🌟 Me/Modding/Game Modding Hub|Game Modding Hub]]

```rust

unsafe{
type FnType = fn(); // type alias to make transmutate easier to read
let address: usize = 0x07FF6A6BA3E00; // the address of the function 
let target: FnType = mem::transmute(address); // transmutate to a function
target(); // calls the function at the address
}
```

Getting from an address to a function call is very unsafe rust-- but is super powerful for stuff like [[🌟 Me/Modding/Hooking|Hooking]].