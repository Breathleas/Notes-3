**指针** 指向一块内存，它的内容是所指内存的地址；引用是某块内存的别名。

**引用** 只能在定义时被初始化一次，之后不可变；指针可变；

引用和指针使用原则：

1. 在可以用引用的情况下，不要用指针；
2. 引用不允许重新赋值.，当使用一个变量指向不同的对象时，必须用指针；
3. 引用不允许为空，当存在对象为空时，必须使用指针。


- 没有变量或对象(引用)的类型是void、有空指针，无空引用、不能用类型来初始化引用、不能建立引用数组、不能建立指向引用的指针/引用。
- 引用没有 const，指针有const，const的指针不可变。