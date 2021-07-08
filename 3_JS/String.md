### 字符串

> #### 1. JS 中字符串是基于 Unicode 编码
>
> [字符编码](http://www.ruanyifeng.com/blog/2007/10/ascii_unicode_and_utf-8.html)

**btoa()**:任意值转为 base64
**atob()**:任意 base64 转为原来的值

> #### 2.1 反斜杠 \
>
> **转义符号**  
> **表示对应的码点**

> #### 2.2 字符串和数组的关系
>
> 字符串是类数组，length 属性返回字符串的长度，且无法改变
> 字符串可以借用数组的方法，返回新的值，但不能在原字符串上进行修改

总结：计算机是如何识别不同语言的？

字符串就是基于这个问题，得到的实现方式。
拓展开来就是 字符串 》 Unicode 编码 ，base64 编码
这里的元知识则是 **字符串编码** 问题
所以这里我真正应该弄懂的是 字符编码的实现