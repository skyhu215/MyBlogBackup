---
layout: post
title: Android 获取系统颜色
date: 2020-05-29 22:12:34
tags: 
 - Android
---


在android中?android与@android有什么区别，可能很少人去纠结这个问题，只是大家在使用上更多的去使用@android:color,  比如给TextView设置颜色
~~~
android:textColor="?android:color/black"
android:textColor="@android:color/black"
~~~
 事实上这两种都是对的，百度上有个回答了这个问题

 ?android与@android的区别是什么？

 android:textAppearance="?android:textAppearanceMedium"
        android:textAppearance="@android:style/TextAppearance.Medium"
不一样吗？？？

不一样，但效果可能一样。 android开发者中有相关说明(Referencing style attributes). @android引用系统资源， ?android 引用本应用theme内的资源。在自定义theme时， 一些未自定义的缺省的属性则相当于引用系统资源

