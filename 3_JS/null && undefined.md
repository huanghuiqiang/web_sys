## null 和 undefined

### 历史

最初只有 null，表示 “无”。可以转换为 0。

> Number(null) // 0

由于 null 是对象，用来表示 “无”，不太合适，报错也不容易发现。就新增了 undefined。

### 区别

1. 不同
   null 表示值，空值。undefined 表示声明了变量，未定义，抛出错误。

2. 相同
   装换为布尔值都是 false

3. undefined 和 undeclared
   （如果未声明变量，直接使用报 is not defined,这个和 undefined 是不一样的。）

4. 问题：

哪些值转换为布尔值是 false？

- 数值： 0, NAN

- 字符串： ''

- 布尔值： false

- null

- undefined

注意： [], {} 转换为布尔值是 true
