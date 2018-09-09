---
title: C++
---

## Introduction

## Memory model

Now this is cleared:

 - variables in a function body are stored on the stack
 - objects created by `new` are stored in the heap (and their address returned)

With examples, to be a bit more visual:

```cpp
void f0() {
		Class* c = new Class();
}

void f1() {
		Class* c = 0;
		c = new Class();
}
```

Here `c` (of type `Class*`) is stored on the stack and points to an object (of type `Class`) that is stored on the heap

```cpp
void f2() {
		Class c = Class();
}

void f3() {
		Class c;
}
```

Here `c` is stored on the stack. In `f2` there *might* be a temporary (object without name) created by the expression `Class()` and then copied into `c` (depending on whether the compiler elides the copy or not), the storage of temporaries is not addressed by the Standard... they commonly use the stack though.

[Ref](https://stackoverflow.com/a/8755644/4446356)
