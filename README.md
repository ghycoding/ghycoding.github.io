### 使用说明

本博客项目是采用hexo & hexo-butterfly主题，本人根据喜好自己配置，clone项目源码后可以自行更改配置。请熟悉hexo搭建流程以及hexo-butterfly主题配置[butterfly文档](https://butterfly.js.org/posts/21cfbf15/)

源码内以及内置了butterfly的主题代码，如需更新主题
```
git clone -b master https://github.com/jerryc127/hexo-theme-butterfly.git themes/butterfly
```

themes\butterfly\source\css目录下新增了custom.css文件，也就是自定义博客样式，本项目只是简单对页面进行了优化。


#### 1、安装依赖
``` 
npm install / cnpm install  
```

#### 2、生成静态文件
```
2、hexo g / hexo generate
```

#### 3、启动服务器。默认情况下，访问网址为： http://localhost:4000/。
```
hexo s / hexo server
```

#### 4、 部署网站。
```
 hexo d / hexo deploy
```
如果hexo失败查看是否安装hexo-deployer 依赖 
```
npm install hexo-deployer-git --save
```



