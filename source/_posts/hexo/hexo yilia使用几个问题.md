---
layout: post
title: hexo guide
tags:
  - hexo
---

## Hexo yilia使用的几个问题



#### 增加归档菜单

修改 `themes/yilia/_config.yml`

```
menu:
    主页:  /
    归档:  /archives/index.html
```



####  添加 categories 到menu菜单

在yilia主题下的主配置文件_config.xml中找到menu,并把categories添加进去

```
menu:
  主页: /
  分类: /categories
  归档: /archives
```



####  hexo yilia主题配置menu不生效

```
1、`_config.yml` 要配置 `yilia` 主题下的，而不是根目录下的 `_config.yml` 文件。

2、修改 `_config.yml` 文件需要重启服务的。`hexo s`
```



#### 文章如何显示摘要

**问题**。点击主页时，发现所有文章都是全文显示，不利于查找，可控制显示的字数

**解决办法**。 在你 MD 格式文章正文插入 <!-- more -->即可，只会显示它之前的，此后的就不显示，点击文章标题，全文阅读才可看到，同时注释掉以下 themes/yilia/_config.yml，重复

```

# excerpt_link: more

```



#### 配置图片资源
添加图片资源文件夹。 路径为 themes/yilia/source/下，可添加一个 assets 文件夹，里面存放图片资源即可

配置文件中直接引用即可。路径为 themes/yilia/_config.yml，找到如下即可

`微信二维码图片`  `weixin:  /assets/img/wechat.png`

`头像图片`  `avatar:  /assets/img/head.jpg`

`网页图标`  `favicon:  /assets/img/head.jpg`


