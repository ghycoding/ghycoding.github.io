---
title: js字符串常见的一些方法
categories:
  - js
abbrlink: 86cd2b6e
date: 2021-05-11 15:53:47
cover: https://images.pexels.com/photos/247791/pexels-photo-247791.png?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260
---

字符串的十四个方法：
charAt(index)、charCodeAt(index)、concat(str, str, ...)、indexOf(item, index)、lastIndexOf(item,index)、substring(stratIndex, stopIndex)、str.substr(start, length) 、split(separator,howmany)、toUpperCase()、toLowerCase()、startsWith()、endsWith()、includes()、repeat（）、trim()、slice()

### 1. str.charAt(n) 返回字符串指定位置的字符
n 如果不在 0~str.length-1之间，则返回一个空字符串

```
var str = 'maomao love you'
str.charAt(3) // m
str.charAt(20) // ''
```

###  2. str.charCodeAt(n) 返回字符串指定位置的字符编码 
```
var str = 'maomao love you'
str.charCodeAt(3) // 109
str.charCodeAt(20) // NaN
```

### 3. concat()方法用于连接两个或多个字符串。

str.concat(stringX,stringX,...,stringX):必需。将被连接为一个字符串的一个或多个字符串对象。
```
var str = '123'
str.concat('牵着手', '456', '抬起头') // "123牵着手456抬起头"
```

### 4. indexOf() 和 lastIndexOf()

返回 value 在字符串 str 中首次出现的位置,从 start 位置开始查找，如果不存在，则返回 -1。value必需。规定需检索的字符串值
str.lastIndexOf(value,fromindex)
返回 value 在字符串 str 中最后出现的位置,从末尾向前开始查找，如果不存在，则返回 -1。

### 5. split()方法用于把一个字符串分割成字符串数组。

```
str.split(separator,howmany)
```
