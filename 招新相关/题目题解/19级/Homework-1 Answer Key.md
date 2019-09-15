# Homework-1 Answer Key

---

## Hello World

### 题目

在IT行业，学习语言的入门就是编写hello world；

今天的作业就是手写一个hello c program的代码。

并且查阅相关资料，尽量解释你写的第一个程序各部分代表什么意思，有什么作用。

### 题解

 ```c
//包含头文件，有了这个才能使用printf函数
#include <stdio.h>
//main 函数， 程序的入口
int main() {
    //  向屏幕输出 “Hello World”
    printf("Hello World");
    // 结束程序
    return 0; 
}
 ```

### FAQ

---

- Q:为什么教科书用的是```main()```或```void main()```， 而给出的题解却是```int main()```呢？

- A:当你浏览一些旧式的C代码时， 会看到以下形式的```main()``` ```void main()```, 一些编译器允许这样写， 但是所有的标准都未认可这样的写法。请坚持使用标准形式```int main()```，这样程序从一个编译器转移到另一个编译器时就不会出现什么问题。