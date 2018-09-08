---
title: Object copy
---

## Introduction

## Shallow copy

將所有的 field 都 copy 一份，如果是 primitive type 直接 copy value，如果是 reference type 就會指向同樣的 object。
以 C++ 為例，pointer 就算是 reference type，default compiler 產生的 copy constructor 和 assign operator 就是使用 shallow copy。
要是使用的 object 都沒有 reference type 就不會有問題，一但有 reference type 的 field 就必須去處理這部分，不然使用 copy 的時候兩個 object 的 reference 會指向同一個 object。

## Deep copy

在 reference type 的 field 會去 dereference 再去複製一份，C++ default compiler 對 container type 的會去 call member 的 copy，像是 vector、string...... 本身的 copy 就是 deep copy。

[Ref](https://en.wikipedia.org/wiki/Object_copying)
