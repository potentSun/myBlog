---
title: JavaScript变量提升
date: 2018-03-13 17:50:29
tags:
- JavaScript
categories:
- JavaScript
---

### 先有鸡还是先有蛋？
举个例子
```js
a = 2;
var a;
console.log(a);  // 2

console.log(b);  // undefined
var b = 2;
```
到底是声明在前，还是赋值在前？
正确的思考思路是，包括变量和函数在内的所有声明都会在任何代码被执行前首先被处理。

以上例子会以如下形式进行处理：
```js
var a;
a = 2;
console.log(a);  // 2

var b;
console.log(b); // undefined
b = 2;
```
要记住，先有声明后有赋值。
只有声明本身会被提升，而赋值或其他运行逻辑会留在原地。
函数声明和变量声明都会被提升，函数会被首先提升，然后才是变量


 