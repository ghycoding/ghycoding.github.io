---
abbrlink: '1'
title: Hexo 生成永久文章链接
cover: false
top: 9
categories:
  - hexo
---

Hexo 默认文章链接生成规则是按照年、月、日、标题来生成的。一旦文章标题或者发布时间被修改，URL 就会发生变化，之前文章地址也会变成 404，而且 URL 层级很深，不利于分享和搜索引擎收录。


## 1.安装
点击即可访问插件源码地址 [hexo-abbrlink](https://github.com/rozbo/hexo-abbrlink) 。

## 配置

修改博客根目录配置文件 _config.yml 的 permalink：

```
# permalink: :year/:month/:day/:title/
permalink: p/:abbrlink.html  # p 是自定义的前缀
abbrlink:
    alg: crc32   #算法： crc16(default) and crc32
    rep: hex     #进制： dec(default) and hex
```


```
hexo clean
hexo g
hexo s
```