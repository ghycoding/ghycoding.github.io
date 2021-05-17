---
title: Vue中数据更新视图不更新解决方法
categories:
  - vue
abbrlink: 9daba997
date: 2021-05-11 15:53:47
cover: https://wallroom.io/img/3840x2160/bg-4186633.jpg
---


在公司做vue项目，数据改变视图不更新，用了$set方法也不好使，为此总结了一些解决这个问题的方法：

1.Vue.$set(target, key, value)； 适用于对象或数组

2.oldObj = Object.assign({}, newObj); 适用于对象（注：oldObj必须是已经声明的对象）

3.push()，pop()，shift()，unshift()，splice()，sort()，reverse()可被vue检测到; 适用于数组

4.Vue.nextTick(callback) （Vue 异步执行 DOM 更新）

5.vue多层循环，动态改变数据后渲染的很慢或者不渲染
可在动态改变数据的方法，第一行加上：this.$forceUpdate();

6.很可能是v-for循环时那个key没有设置为唯一值，最好别设置为索引；（数据结构层级嵌套比较深一定要注意，本人就踩过坑）

7.先赋值为null，然后Vue.nextTick(callback)重新赋值正确的数据(这个稍微有点暴力哈。。。),有时候上面几种方法都不管用时可以试试
