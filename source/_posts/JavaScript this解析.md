---
title: JavaScript this解析
date: 2018-03-15 17:18:00
tags:
- JavaScript
categories:
- JavaScript
---

### 理解调用位置
调用位置就是函数在代码中被调用的位置（不是声明时的位置）

举个例子
```js
    function baz(){
        //当前调用栈是： baz
        //调用位置是全局作用域
        console.log("baz");
        bar(); 
    }

    function bar(){
        //当前调用栈是： baz -> bar
        //调用位置是在 baz中
        console.log("bar");
        foo(); 
    }

    function foo(){
        //当前调用栈是： baz -> bar -> foo
        //调用位置是在 bar中
        console.log("foo"); 
    }

    baz();
```

### 绑定规则
1.默认绑定
2.隐式绑定
3.显式绑定
4.new绑定

