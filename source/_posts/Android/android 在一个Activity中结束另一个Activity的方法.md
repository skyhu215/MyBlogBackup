---
layout: post
title: android 在一个Activity中结束另一个Activity的方法
date: 2020-05-29 22:12:34
tags: 
 - Android
---



下面以ActivityB结束ActivityA为例

1、首先在ActivityA中定义一个静态的全局变量

static Activity ActivityA；



2、在ActivityA中的onCreate方法中给ActivityA赋值

ActivityA = this；



3、在ActivityB中，需要结束ActivityA时调用

ActivityA a = new ActivityA();a.ActivityA.finish();