---
layout: post
title: npm 使用国内淘宝镜像方法
date: 2020-05-22 23:55:20
tags:
 - JavaScript
---


### npm使用国内淘宝镜像的方法

一.通过命令配置

1. 命令

npm config set registry https://registry.npm.taobao.org

2. 验证命令

npm config get registry   如果返回https://registry.npm.taobao.org，说明镜像配置成功。

<!-- more -->


二、通过使用cnpm安装

1. 安装cnpm

npm install -g cnpm --registry=https://registry.npm.taobao.org

2. 使用cnpm

cnpm install  库名称