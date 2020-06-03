---
layout: post
title: Android Studio引用jar及so文件
date: 2020-05-29 22:12:34
tags: 
 - Android
---



在网上看到讲解android studio讲解jar和so文件添加的方法，觉得写的很好，所以摘抄下来目地是让自己记住这种添加方式，自己实践了也验证了正确性。[Android Studio开发入门-引用jar及so文件](http://www.cnblogs.com/xrwang/p/AndroidStudioImportJarAndSoLibrary.html)	
    

**一、引用jar文件**
    1.将jar文件复制、粘贴到app的libs目录中；
    2.右键点击jar文件，并点击弹出菜单中的“Add As Library”，将jar文件作为类库添加到项目中；
    3.选择指定的类库。
    注：如果不执行2、3步，jar文件将不起作用，并且不能使用import语句引用。    ![img](http://images.cnitblog.com/i/21602/201405/011028264559301.png)



二、引用so文件**
    网上有很多引用so文件的方法，多数都很麻烦，在KYLE THIELK的博客中找到了一种简单的方法。
    1.在“src/main”目录中新建名为“jniLibs”的目录；
    2.将so文件复制、粘贴到“jniLibs”目录内。
    注：如果没有引用so文件，可能会在程序执行的时候加载类库失败，有类似如下的DEBUG提示：
    java.lang.UnsatisfiedLinkError: Couldn't load library xxxx from loader dalvik.system.PathClassLoader    ![img](http://images.cnitblog.com/i/21602/201405/011028520642193.png)





三、致谢及源代码下载**
    感谢您看完本文，希望对您有帮助。
    源代码是使用百度语音识别引擎的例子，[点击这里下载](http://files.cnblogs.com/xrwang/AndroidTestProject.rar)。
    注：1.本文使用的Android Studio版本为0.4.6；
    2.API KEY及安全KEY我随便改了个，您需要替换成自己申请的KEY才能正常运行；

 Android Studio开发入门-引用jar及so文件 - Wuya - 博客园      
[Android Studio开发入门-引用jar及so文件](http://www.cnblogs.com/xrwang/p/AndroidStudioImportJarAndSoLibrary.html)		     作者：王先荣
    最近初学安卓开发，因为以前从未用过JAVA，连基本的语法都要从头开始，所以不太顺利。在尝试使用百度语音识别引擎时遇到了如何引用jar及so文件的问题。在GOOGLE加多次尝试之后，找到了一个比较简单的方法，特介绍如下。

一、引用jar文件**
    1.将jar文件复制、粘贴到app的libs目录中；
    2.右键点击jar文件，并点击弹出菜单中的“Add As Library”，将jar文件作为类库添加到项目中；
    3.选择指定的类库。
    注：如果不执行2、3步，jar文件将不起作用，并且不能使用import语句引用。    ![img](http://images.cnitblog.com/i/21602/201405/011028264559301.png)



二、引用so文件**
    网上有很多引用so文件的方法，多数都很麻烦，在KYLE THIELK的博客中找到了一种简单的方法。
    1.在“src/main”目录中新建名为“jniLibs”的目录；
    2.将so文件复制、粘贴到“jniLibs”目录内。
    注：如果没有引用so文件，可能会在程序执行的时候加载类库失败，有类似如下的DEBUG提示：
    java.lang.UnsatisfiedLinkError: Couldn't load library xxxx from loader dalvik.system.PathClassLoader    ![img](http://images.cnitblog.com/i/21602/201405/011028520642193.png)



**三、致谢及源代码下载**
    感谢您看完本文，希望对您有帮助。
    源代码是使用百度语音识别引擎的例子，[点击这里下载](http://files.cnblogs.com/xrwang/AndroidTestProject.rar)。
    注：1.本文使用的Android Studio版本为0.4.6；
    2.API KEY及安全KEY我随便改了个，您需要替换成自己申请的KEY才能正常运行；
    3.参考网址：[http://www.kylethielk.com/blog/include-native-so-library-in-apk-with-android-studio/](http://www.kylethielk.com/blog/include-native-so-library-in-apk-with-android-studio/)