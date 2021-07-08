## 一.数据类型

数据类型在语言中，用来作为容器，存储数据

### 原始数据类型（primitive）

- 数字，计算
- 布尔值，判断
- 字符串，展示

### 合成数据类型(complex)

- 对象
  - 数组
  - 函数
  - 狭义的对象

### 特殊值

- undefined
- null

## 二.判断数据类型的方法

1. typeof 运算符

2. instanceof 运算符

3. Object.prototype.toString 方法

`typeof 123 // "number"`

`typeof true // "boolean"`

`typeof 'abc' // "string"`

`typeof {} // "object"`

`typeof [] // "object"`

数组是对象的一种

`typeof undefined // "undefined"`

用来检查一个变量是否声明了

`typeof null // "object"`

历史问题，第一版语言，把 null 作为了对象。现在为了兼容以前的代码，保留了

## 问题

1. 如何判断一个变量是不是对象（狭义的对象）？

let key = {}

typeof key === "object" && !(key instanceof Array) && key !== null

Object.prototype.toString.call(key) === "object object"
