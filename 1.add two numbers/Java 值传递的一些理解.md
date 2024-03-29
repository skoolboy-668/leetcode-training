**Java 值传递的一些理解**

1. **搞清楚 基本类型和引用类型的不同之处**

   基本类型，值是直接保存在变量中

   引用类型，变量中保存的是实际对象的地址，一般称这种变量为 引用， 引用指向实际对象，实际对象中保存着内容

2. **赋值运算符（=）的作用**

   对于基本类型，赋值运算符直接改变变量的值，原来的值被覆盖掉

   对于引用类型，**赋值运算符是改变了变量里面存储的地址，原来的地址被覆盖掉，但是原来的对象不会被覆盖**，没有任何引用指向的对象是垃圾，会被GC

3. **函数调用**

   **赋值一份当前的变量值，里面可能是实际的变量值（基本类型），也可能是地址值（引用类型）。**

   如果在调用的函数里面new了一个对象，那么形参里面的地址就要改变，原来的不变。

   如果调用的函数里面没有新建对象，而是直接对地址指向的对象进行修改，原变量同时也是指向这个地址，他里面的值自然是有变化的