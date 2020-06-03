---
layout: post
title: Android 5x
date: 2020-05-29 22:12:34
tags: 
 - Android
---


###### Toast 中使用Contrext 是使用Application的Context好 还是Activity的Context好

---

###### 多个请求的时候 进度条怎么显示 是一个一个显示还是只显示第一个

---

###### AlarmManager 是什么东西

----

###### IntentService 和Service有什么不同

---

###### Java静态代码块static执行顺序

---

###### android自定义view

---

###### File 文件流

---

###### view.getViewTreeObserver().addOnGlobalLayoutListener

---

###### 图片的信息exif 信息

---

###### MarkDown 语法

---



###### 、IOException

---

######  android:drawableLeft="@drawable/icon_about" 

---

###### 如何把从服务器获取的名字匹配drawable里的图片？如：（网络获取的名字“展示”，从drawable里获取相应的图片（zhanshi.png））  反射去获取

这个方法就是通过反射获取指定图片名字的资源Id的方法

public static int getDrawableResourceId(String name){

 try(){

Field field=R.drawable.class.getField(name);

return  field.getInt（null);

}catch(NoSuchFieldException e)

e.printStackTrace();  

}catch(IllegalAccessException e)

e.printStackTrace();  

}catch(IllegalAragumentException e)

e.printStackTrace();  

}

return -1;

---

###### MeasureSpec.UNSPECIFIED 和almost、extra区别

---

###### Android  5.x Material Design设计风格

1.Android5.x新特性之 RecyclerView/CardView/Palette/FloatButton

	dependencies {
	    compile fileTree(include: ['*.jar'], dir: 'libs')
	    compile 'com.android.support:recyclerview-v7:21.0.3'
	    compile 'com.android.support:cardview-v7:21.0.3'
	    compile 'com.android.support:palette-v7:22.2.0'
	}

1. Android5.x新特性之 Toolbar和Theme的使用

3.谷歌推出了Android Design Support Library 库，全面支持MD设计风格的UI效果。Design Support Library库吸收了8 个新的 material design 组件！最低支持 Android2.1，其实很多组件都是Github上比较火的，只是谷歌把它官方化了，便于开发者使用。今天我们来学习
FloatingActionButton，TextInputLayout，Snackbar，TabLayout 四种控件。

 这篇博客我们继续学习Design库中的其他四个组件，分别是AppBarLayout，NavigationView，CoordinatorLayout，CollapsingToolbarLayout。同样，你需要在你的工程中引入
compile 'com.android.support:design:22.2.0'

Drawerlayout和NavigationView实现优雅的Google范儿侧边栏

总的来说：AppBarLayout、CollapsingToolbarLayout、CoordinatorLayout、FloatingActionButton、NavigationView、Snackbar、TabLayout、TextInputLayout、

###### listview

  <com.welearn.banzhuren.view.XListView
        android:id="@+id/answer_list"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:cacheColorHint="@android:color/transparent"
        android:divider="@color/answer_list_diver"
        android:fadingEdge="none"
        android:fastScrollEnabled="false"
        android:footerDividersEnabled="false"
        android:headerDividersEnabled="false"
        android:listSelector="@android:color/transparent"
        android:scrollbars="none" />

---

###### notification和notification.Builder()
***
######自定义属性的使用
做Android布局是件很享受的事，这得益于他良好的xml方式。使用xml可以快速有效的为软件定义界面。可是有时候我们总感觉官方定义的一些基本组件不够用，自定义组件就不可避免了。那么如何才能做到像官方提供的那些组件一样用xml来定义他的属性呢？现在我们就来讨论一下他的用法。

一、在res/values文件下定义一个attrs.xml文件，代码如下：

<?xml version="1.0" encoding="utf-8"?> 
<resources> 
    <declare-styleable name="ToolBar"> 
        <attr name="buttonNum" format="integer"/> 
        <attr name="itemBackground" format="reference|color"/> 
    </declare-styleable> 
</resources>

二、在布局xml中如下使用该属性:

<?xml version="1.0" encoding="utf-8"?> 
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android" 
    xmlns:toolbar="http://schemas.android.com/apk/res/cn.zzm.toolbar" 
    androidrientation="vertical" 
    android:layout_width="fill_parent" 
    android:layout_height="fill_parent" 
    > 
    <cn.zzm.toolbar.ToolBar android:id="@+id/gridview_toolbar" 
        android:layout_width="fill_parent" 
        android:layout_height="wrap_content" 
        android:layout_alignParentBottom="true" 
        android:background="@drawable/control_bar" 
        android:gravity="center" 
        toolbar:buttonNum="5" 
        toolbar:itemBackground="@drawable/control_bar_item_bg"/> 
</RelativeLayout>

三、在自定义组件中，可以如下获得xml中定义的值：

TypedArray a = context.obtainStyledAttributes(attrs,R.styleable.ToolBar); 
buttonNum = a.getInt(R.styleable.ToolBar_buttonNum, 5); 
itemBg = a.getResourceId(R.styleable.ToolBar_itemBackground, -1);

a.recycle();

就这么简单的三步，即可完成对自定义属性的使用。

*********************************************************************

好了，基本用法已经讲完了，现在来看看一些注意点和知识点吧。

首先来看看attrs.xml文件。

该文件是定义属性名和格式的地方，需要用<declare-styleable name="ToolBar"></declare-styleable>包围所有属性。其中name为该属性集的名字，主要用途是标识该属性集。那在什么地方会用到呢？主要是在第三步。看到没？在获取某属性标识时，用到"R.styleable.ToolBar_buttonNum"，很显然，他在每个属性前面都加了"ToolBar_"。

在来看看各种属性都有些什么类型吧：string , integer , dimension , reference , color , enum.

前面几种的声明方式都是一致的，例如：<attr name="buttonNum" format="integer"/>。 
只有enum是不同的，用法举例：

<attr name="testEnum"> 
    <enum name="fill_parent" value="-1"/> 
    <enum name="wrap_content" value="-2"/> 
</attr>

如果该属性可同时传两种不同的属性，则可以用“|”分割开即可。



让我们再来看看布局xml中需要注意的事项。

首先得声明一下：xmlns:toolbar=http://schemas.android.com/apk/res/cn.zzm.toolbar 
注意，“toolbar”可以换成其他的任何名字，后面的url地址必须最后一部分必须用上自定义组件的包名。自定义属性了，在属性名前加上“toolbar”即可。



最后来看看java代码中的注意事项。

在自定义组件的构造函数中，用

TypedArray a = context.obtainStyledAttributes(attrs,R.styleable.ToolBar);

来获得对属性集的引用，然后就可以用“a”的各种方法来获取相应的属性值了。这里需要注意的是，如果使用的方法和获取值的类型不对的话，则会返回默认值。因此，如果一个属性是带两个及以上不用类型的属性，需要做多次判断，知道读取完毕后才能判断应该赋予何值。当然，在取完值的时候别忘了回收资源哦！

***
###### 自定义控件的一些api 
Paint:
canvas:
rect:
onMeasure()-->widthMeasureSpec
onDraw()-->heightMeasureSpec
getMeasuredWidth(), getMeasuredHeight()




######   单例类传入context，context有回调的时候内存泄露问题


###### uri和url的区别



















​    