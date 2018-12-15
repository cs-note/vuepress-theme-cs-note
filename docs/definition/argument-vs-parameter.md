---
title: argument vs parameter
---

argument 是 function 外傳入的參數
parameter 是 function 內收到的參數


``` c
int func(int parameter){
    return parameter;
}
int main(){
    int argument = 1;
    func(argument);
}
```
