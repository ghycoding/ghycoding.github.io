---
title: javaScript
categories:
  - web
date: 2021-05-11 15:53:47
top: 1
abbrlink: 86cd
cover: https://images.pexels.com/photos/240163/pexels-photo-240163.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500
---

## 每日一题

<!-- 第1题 -->
<details>
<!-- 标题 -->
<summary style="margin-bottom:8px"><b>1. document load 和 document ready 的区别</b></summary>
答案：页面加载完成有两件事情<br/>
1、load是当页面所有资源全部加载完成后（包括DOM文档树，css文件，js文件，图片资源等），执行一个函数。
问题：如果图片资源较多，加载时间较长。onload后等待执行的函数等到时间较长，所以一些效果受到影响。<br/>
2、$(document).ready()s DOM文档树加载完成之后执行一个函数（不含图片，css等）所有会比onload较快执行，在原生的js中不包括ready（）这个方法，只有load方法，也就是onload事件
</details>

<!-- 第2题 -->
<details>
<summary style="margin-bottom:8px"><b>2. JavaScript 中如何检测一个变量是一个 String 类型？</b></summary>
答案：四种方法（typeof、constructor、instanceof、Object.prototype.toString.call()）

```js
var str = 'I am xiaogao'

1. typeof
      typeof(str) => 'string'  // typeof  返回的是一个类型
      type str => 'string'

2. constructor  /*（constructor 是prototype对象上的属性，指向构造函数。
根据实例对象寻找属性的顺序，若实例对象没有实例属性或者方法时，就是原型链上找）*/
      str.constructor   =>   ƒ String() { [native code] }
      str.constructor == String    //true

3. instanceof
      new String('sdsda').instanceof // true
      str.instanceof String // false 
      /* 以上形式的Number，String，Boolean判断不出类型，但如果使用new新建，则可以检测出
      null和undefined返回false，因为它们的类型就是自己本身，不是object创建出来的，所以返回false */

4. Object.prototype.toString.call()
      Object.prototype.toString.call('123') === '[object String]' // true
```
</details>

<!-- 第3题 -->
<details>
<summary style="margin-bottom:8px"><b>3.请用 js 去除字符串空格？</b></summary>
答：有以下几种方式  replace 正则匹配方法、str. trim()方法、JQ 方法：$. trim(str)方法
<br/>
方法一：replace 正则匹配方法<br/>

```js
去除字符串内所有的空格：str = str. replace(/\s*/g, "");
去除字符串内两头的空格：str = str. replace(/^\s*|\s*$/g, "");
去除字符串内左侧的空格：str = str. replace(/^\s*/, "");
去除字符串内右侧的空格：str = str. replace(/(\s*$)/g, "");
```
<br/>
方法一：str. trim()方法<br/>
trim()方法是用来删除字符串两端的空白字符并返回，trim 方法并不影响原来的字符串本身，它返回的是一个新的字符串。
缺陷：只能去除字符串两端的空格，不能去除中间的空格

```js
var str = " 6 6 ";
var str_1 = str.trim();
console.log(str_1); //6 6//输出左右侧均无空格
```
<br/>
方法三：JQ 方法：$. trim(str)方法<br/>

```js
var str = " 6 6 ";
var str_1 = $.trim(str);
console.log(str_1); //6 6//输出左右侧均无空格
```
</details>