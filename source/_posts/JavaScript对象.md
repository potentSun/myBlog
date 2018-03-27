---
title: JavaScript对象
date: 2018-03-27 00:13:59
tags:
- JavaScript
categories:
- JavaScript
---
### JavaScript语法
对象可以通过两种形式定义：声明(文字)形式和构造形式。
```js
    var myObj = { //声明形式
        age: 18
    }; 

    vat myObj = new object(); //构造形式
    myObj.age = 18; 

    多数情况下都会使用第一种形式
```

### JavaScript类型
对象是JavaScript的基础，在JavaScript中一共有六种数据类型

1.string
2.number
3.boolean
4.null
5.undefined
6.object

在ES6里新定义了一种数据类型Symbol算是第七种

注意null比较特殊,有时会被当做一种对象类型,typeof null的时候,会返回字符串"object",实际上null只是基本类型

这个问题的原理是这样的 
不同的对象在底层中都表示二进制，在JavaScript中二进制前三位都为0的话会被判断为object类型,null的二进制表示全是0,
所以在执行typeof的时候会返回"object"

### 内置对象
1.String
2.Number
3.Boolean
4.Object
5.Function
6.Array
7.Date
8.RegExp
9.Error

### 属性描述符
```js
    var myObj = {
        age: 18
    };

    Object.getOwnProperDescriptor(myObj,"age");
    // {
    //     value: 18,
    //     writable: true,
    //     configurable: true,
    //     enumberable: true
    // }
```
writable(可写)  configurable(可配置)  enumberable(可枚举)




