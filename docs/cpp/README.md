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

## vector

像是 dynamic array 一樣能提供快速的 random access，實作是分配一塊連續的記憶體空間，當不夠時會重新分配另一塊記憶體空間，並將原本的元素複製過去，因為實作是array，當 insert 元素在結尾以外的地方會非常沒有效率。

### Time complexity

| Operation | Big O |
|-----------|--------------------------------------|
| access | O(1) |
| push_back | O(1)，如果超過原本的容量就會到達O(n) |
| pop_back | O(1) |
| insert | O(number of inserted elements) + O(number of elements after insert position) |
| erase | O(number of erased elements) + O(number of elements after erased position) |

