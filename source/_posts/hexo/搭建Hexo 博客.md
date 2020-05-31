---
layout: post
title: 搭建Hexo博客
date: 2020-05-23 00:39:51
tags:
  - hexo
---



- [hexo 博客搭建](#hexo-%e5%8d%9a%e5%ae%a2%e6%90%ad%e5%bb%ba)
    - [安装Node.js](#%e5%ae%89%e8%a3%85nodejs)
    - [安装cnpm](#%e5%ae%89%e8%a3%85cnpm)
    - [全局安装hexo框架](#%e5%85%a8%e5%b1%80%e5%ae%89%e8%a3%85hexo%e6%a1%86%e6%9e%b6)
    - [建立一个博客文件夹](#%e5%bb%ba%e7%ab%8b%e4%b8%80%e4%b8%aa%e5%8d%9a%e5%ae%a2%e6%96%87%e4%bb%b6%e5%a4%b9)
    - [使用命令初始化博客](#%e4%bd%bf%e7%94%a8%e5%91%bd%e4%bb%a4%e5%88%9d%e5%a7%8b%e5%8c%96%e5%8d%9a%e5%ae%a2)
    - [本地访问博客](#%e6%9c%ac%e5%9c%b0%e8%ae%bf%e9%97%ae%e5%8d%9a%e5%ae%a2)
    - [创建一篇文章](#%e5%88%9b%e5%bb%ba%e4%b8%80%e7%af%87%e6%96%87%e7%ab%a0)
    - [用cd命令退回到目录blog](#%e7%94%a8cd%e5%91%bd%e4%bb%a4%e9%80%80%e5%9b%9e%e5%88%b0%e7%9b%ae%e5%bd%95blog)
- [将博客部署到github上面去 通过地址访问](#%e5%b0%86%e5%8d%9a%e5%ae%a2%e9%83%a8%e7%bd%b2%e5%88%b0github%e4%b8%8a%e9%9d%a2%e5%8e%bb-%e9%80%9a%e8%bf%87%e5%9c%b0%e5%9d%80%e8%ae%bf%e9%97%ae)
    - [登录github账号](#%e7%99%bb%e5%bd%95github%e8%b4%a6%e5%8f%b7)
    - [新建一个仓库](#%e6%96%b0%e5%bb%ba%e4%b8%80%e4%b8%aa%e4%bb%93%e5%ba%93)
    - [在myblog 目录下安装git插件](#%e5%9c%a8myblog-%e7%9b%ae%e5%bd%95%e4%b8%8b%e5%ae%89%e8%a3%85git%e6%8f%92%e4%bb%b6)
    - [保存退出](#%e4%bf%9d%e5%ad%98%e9%80%80%e5%87%ba)
    - [接下来的事情就是部署到远端了 部署命令](#%e6%8e%a5%e4%b8%8b%e6%9d%a5%e7%9a%84%e4%ba%8b%e6%83%85%e5%b0%b1%e6%98%af%e9%83%a8%e7%bd%b2%e5%88%b0%e8%bf%9c%e7%ab%af%e4%ba%86-%e9%83%a8%e7%bd%b2%e5%91%bd%e4%bb%a4)
    - [使用xx.github.io 访问](#%e4%bd%bf%e7%94%a8xxgithubio-%e8%ae%bf%e9%97%ae)
- [关于博客主题  更换主题](#%e5%85%b3%e4%ba%8e%e5%8d%9a%e5%ae%a2%e4%b8%bb%e9%a2%98-%e6%9b%b4%e6%8d%a2%e4%b8%bb%e9%a2%98)
    - [进入myblog目录,克隆主题](#%e8%bf%9b%e5%85%a5myblog%e7%9b%ae%e5%bd%95%e5%85%8b%e9%9a%86%e4%b8%bb%e9%a2%98)
    - [修改配置文件](#%e4%bf%ae%e6%94%b9%e9%85%8d%e7%bd%ae%e6%96%87%e4%bb%b6)



## hexo 博客搭建

#### 安装Node.js

从Node.js 官网安装Node.js ,下载Node.js安装包安装,安装完Node.js电脑就会有Node 环境和 NPM

<!-- more -->

#### 安装cnpm

```
npm install -g cnpm --registry=https://registry.npm.taobao.org

用 cnpm -v 检测cnpm是否安装成功
```

#### 全局安装hexo框架 

```
cnpm install -g  hexo-cli
安装完hexo 后用 hexo -v 验证版本
```


#### 建立一个博客文件夹

```
mkdir  myblog
```


#### 使用命令初始化博客

```
cd myblog
sudo hexo init
```


#### 本地访问博客 
hexo s

```
Start Processing
Hexo is running at http://localhost:4000. Press Ctrl+C to stop
```

#### 创建一篇文章
hexo n "我的第一篇md"

进入目录到刚才创建文档的页面 路径为 E:\github\myblog\source\_posts\

编辑md文档，录入自己想要输入的内容  可以尝试用vscode或者typora等工具编辑文档

保存 退出

#### 用cd命令退回到目录blog  
hexo clean  清理下项目
hexo g     生成

hexo s  预览页面







## 将博客部署到github上面去 通过地址访问

#### 登录github账号

#### 新建一个仓库  
    -  注意仓库地址名称 git用户名.github.io   必须是git用户名称

    - 描述：我的hexo博客

#### 在myblog 目录下安装git插件

  ```
  cnpm install  --save  hexo-deployer-git
  
  ```

  - 打开myblog目录下面的_config.yml 编辑之

  - 文件底部 找到节点 deploy 格式如下
  ```
  deploy:
     type:git
     repo: https://github.com/xxx/xx.github.io
     branch:master

  ```

#### 保存退出

#### 接下来的事情就是部署到远端了 部署命令
  
  hexo d

  过程中输入github账号和密码 这样就可以向远端推送代码了  出现Deploy Done部署成功 快去刷新下github页面看看文件是不是都推送到github上面去了 哈哈哈...


#### 使用xx.github.io 访问




##  关于博客主题  更换主题

推荐安装主题   github.com/litten/hexo-theme-yilla

#### 进入myblog目录,克隆主题

git clone https://github.com/litten/hexo-theme-yilia.git     /themes/yilia


#### 修改配置文件

cd themes/

回到myblog目录 进入配置文件 _config.yml   找到theme节点 修改landscape-->yilia  保存退出

hexo  clean
hexo g
hexo s

hexo d 推动到远端

过几分钟访问 https://xx.github.io 访问了







