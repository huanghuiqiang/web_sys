## 一.TyepScript 和 JavaScript 的区别
使用 JS ，大部分错误都是在运行时发现。弱类型
使用 TS，在静态代码发现就能发现其中一些错误。强类型

## 语言类型区别
JavaScript： 弱类型

TypeScript:  强类型
## 二.TypeScript的类型
### 1.number: 
```
let decLiteral: number = 6;
let hexLiteral: number = 0xf00d;
let binaryLiteral: number = 0b1010;
let octalLiteral: number = 0o744;
```
### 2.String
```
let name: string = "bob";
name = "smith";
```
### 3.array
所有元素类型值，相同的集合
```
let list: number[] = [1, 2, 3];
let list: Array<number> = [1, 2, 3];
```
### 4.Boolean
```
let isDone: boolean = false;
```
### 5.Function
声明参数类型和返回的类型
### 6.any
不会做类型检查
### 7.viod
表示函数不返回任何值或者undefined
### 8.object
### 9.tuple
数量固定，类型可以各异
```
const [users, setUsers] = useState([]);
```
### 10.enum
```
enum Direction {
    Up = 1,
    Down,
    Left,
    Right
}
```
数字枚举：定义了一个数字枚举， Up使用初始化为 1。 其余的成员会从 1开始自动增长
### 11.null和undefined
```
// Not much else we can assign to these variables!
let u: undefined = undefined;
let n: null = null;
```
### 12.unknown
表示这个值是可以任何值。和any比，是严格版本
intergace
使用上面的基本类型，创建一个自定义类型
## 三.TypeScript的类型推论
初始化变量的时候，自动设置类型
let x = 3;
.d.ts
让JS文件保持自己JS文件的身份，而拥有TS类型的保护。
## 四.TypeScript的泛型
在TypeScript使用泛型创建工厂函数时，需要引用构造函数的类类型
```
function identity<T>(arg: T): T {
    return arg;
}
```
## 箭头函数的泛型写法
```
const foo = <T, >(x: T) => x;
const foo = <T extends unknown>(x: T) => x;
function foo<T>(x: T): T { return x; }
```