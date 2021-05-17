---
title: 网页布局-CSS定位
cover: https://images.pexels.com/photos/6212801/pexels-photo-6212801.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260
categories:
  - css
abbrlink: 9daba998
date: 2021-05-11 15:53:47
---

### CSS 定位的基本类型（position）

position 属性用来指定一个元素在网页上的位置，一共有 5 种定位方式，即 position 属性主要有五个值。

#### 1.static (默认值)

+ static 是 position 属性的默认值。如果省略 position 属性，浏览器就认为该元素是 static 定位。
+ 这时浏览器会按照源码的顺序，决定每个元素的位置，这称为"正常的页面流"（normal flow）。每个块级元素占据自己的区块（block），元素与元素之间不产生重叠，这个位置就是元素的默认位置。
+ 该关键字指定元素使用正常的布局行为，即元素在文档常规流中当前的布局位置。此时  top, right, bottom, left  和  z-index  属性无效;

#### 2.相对定位(relative)

+ 相对定位就是相对于自己以前在标准流中的位置（即 static 时的位置）来移动；它必须搭配 top、bottom、left、right 这四个属性一起使用，用来指定偏移的方向和距离；

注意点:

 + 由于相对定位是不脱离标准流的, 所以在相对定位中是区分块级元素/行内元素/行内块级元素
 + 由于相对定位是不脱离标准流的, 并且相对定位的元素会占用标准流中的位置, 所以当给相对定位的元素设置 margin/padding 等属性的时会影响到标准流的布局

应用场景：

1 用于对元素进行微调
2 配合后面学习的绝对定位来使用


...........


