---
{"dg-publish":true,"permalink":"/rust-function-addresses-to-function-calls/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowLocalGraph":true}
---

#cs #rust #modding 
> [[Game Modding Hub|Game Modding Hub]]

```rust

unsafe{
type FnType = fn(); // type alias to make transmutate easier to read
let address: usize = 0x07FF6A6BA3E00; // the address of the function 
let target: FnType = mem::transmute(address); // transmutate to a function
target(); // calls the function at the address
}
```

Getting from an address to a function call is very unsafe rust-- but is super powerful for stuff like [[Hooking|Hooking]].