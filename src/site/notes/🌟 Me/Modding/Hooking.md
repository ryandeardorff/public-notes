---
{"dg-publish":true,"permalink":"/me/modding/hooking/","dgHomeLink":true,"dgPassFrontmatter":false}
---

# Hooking
#cs #modding 
> [[🌟 Me/Modding/Game Modding Hub|Game Modding Hub]], [[DLL Injection|DLL Injection]]

**tldr:** You replace a function in an executable with a call to someplace else and rebuild/replace the functionality there. You can do this in memory while the application is running, and it can work in conjunction with [[DLL Injection|DLL Injection]] to non-destructively change the behavior of a program at runtime.
Great article on the subject: [Kyle Halladay - X64 Function Hooking by Example](http://kylehalladay.com/blog/2020/11/13/Hooking-By-Example.html)

### What is it?
Hooking is the process of injecting/patching additional code in place of/in addition to existing code in an executable. There's a bunch of different techniques involved to do this, and various different situations where it could be useful.

#### Hooking and modding
Hooking an x86 or x86_64 executable at runtime is one way of creating scripting mods and changing the functionality of a program-- not just the data going into and out of it.
The basic idea is to replace in memory the instructions of the function with a call to an outside function, then replace or reconstruct the original functionality there-- that way you aren't confined to the same size footprint of the original function. Even doing this can have a number of challenges, and the article [Kyle Halladay - X64 Function Hooking by Example](http://kylehalladay.com/blog/2020/11/13/Hooking-By-Example.html) describes the whole process excellently.