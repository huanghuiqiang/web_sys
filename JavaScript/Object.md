### 对象

> #### 1.1 对象是 JS 中的核心概念

1.2 键名都是字符串，需要符合标识名的条件
1.3 键名又叫做属性，键值可以是任意数据类型，
键值如果是函数，这个属性被称为“方法”
1.4 不同的变量名指向同一个地址，都是对这个对象的引用

{}, 里面一律解释为代码块（语句）
(), 里面只能是表达式
如果需要解释为对象，要这样写，({foo: 123})

### 面向对象

new 命令总是返回一个对象，要么是实例对象，要是是 return 中指定的对象

this 在很多场合使用，但总是返回一个对象。
this 就是函数运行时候所在的对象（环境）。
JS 支持运行环境动态切换，没法事先确定指向哪个对象。

JS 中的对象是个很神奇的东西，万物皆是对象。
所以要理解构造函数，原型对象，实例对象，this，继承，这些东西，都要放到 JS 中是如何通过内存保存对象，这一基础设定下来看待。因为后面那些都是这个的衍生问题的解决方法。

JS 中的对象是保存在一块内存中，把内存地址赋值给变量，调用的时候都是通过不断读取地址，进行引用。由于 JS 中的函数，可以作为变量的值，作为属性的值，这些都是通过赋值实现的。但这也导致了一个问题，函数执行的时候，无法知道当前是在哪个环境中执行（这里因为环境也都是对象，函数直接执行，在浏览器中就是指的 window 对象，如果是作为属性的方法被调用，在则是在狭义对象中被执行）。作用域分为全局作用域和函数作用域，函数内部是可以读取外部的变量。因而需要一个办法，用来在函数内部判断当前是在哪个环境中执行。this 就是被设计来指代当前环境变量，总是返回一个对象。

这里涉及到了很多知识，内存管理，址引用，作用域

new 命令本质也是一个函数，1.创建一个空对象 2.然后把空对象的原型，指向构造函数的 prototype 属性，3.将这个空对象赋值给 this 4. 执行构造函数内部的代码 5.最后会返回 this 对象

### 为什么设计 this？

函数可以在不同的环境对象下运行，需要一种机制能够在函数内区别当前运行环境。
this 就是被设计用来指代函数当前的运行环境

定义在 Object.prototype 对象上面的属性和方法，将被所有实例对象共享

Object 不仅可以当做工具函数使用（将其他类型的值，转成对象），还能当做构造函数使用

this
