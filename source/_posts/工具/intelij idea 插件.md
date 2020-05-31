---
layout: post
title: Intelij idea 插件
date: 2020-05-29 22:08:01
tags:
  - 工具
---

**1、Free-idea-mybatis**

mybatis xml和对应的mapper之间来回切换的时候，有时候不同人开发，放置的位置又不同，使用此插件后，来回切换的时候异常方便，和所放置的位置无关~





**2.翻译插件Translation**

开发的时候经常会遇到看不懂的英语单词，再去百度多麻烦，这里推荐这款翻译插件，插件名称叫做，安装后选中单词按下快捷键ALT+1即可。


<!-- more -->



**3.Maven Helper**

主要功能如下：查找和排除冲突依赖项的简便方法，为包含当前文件或根模块的模块运行/调试maven目标的操作，运行/调试当前测试文件的操作





**4、Lombok**

Lombok能以简单的注解形式来简化java代码，提高开发人员的开发效率。例如开发中经常需要写的javabean，都需要花时间去添加相应的getter/setter，也许还要去写构造器、equals等方法，而且需要维护，当属性多时会出现大量的getter/setter方法，这些显得很冗长也没有太多技术含量，一旦修改属性，就容易出现忘记修改对应方法的失误。Lombok能通过注解的方式，在编译时自动为属性生成构造器、getter/setter、equals、hashcode、toString方法。

出现的神奇就是在源码中没有getter和setter方法，



**5、IdeaJad**

以前查看class文件形式的时候或者jar，都会使用一个外部反编译工具，这样操作明显不方便，使用此插件可以一直在idea中查看文件~  ps：其实Inteli Idea这个编译器已经自带了反编译功能，老夫~~~~~~

选择class文件，右键 Decompile,完成反编译





**6、GrepConsole**

Idea console输出日志一大推，想要快速找到自己想要的类型日志，使用此插件可以快速定位到自己关注的类型日志，比如error，warn，自己也可以配置自己喜欢的颜色~

从settings进入，点击 other settings，可以配置自己喜欢的颜色提示，比如我只选择了默认~



**7、GsonFormat**

在与组外或者不同部门对接接口时候发现，有时候对方返回的是JSON对象，自己想要用一个对象去接受，以便于处理后续，此时，需要自己一个个手动去输入属性么，肯定很抓狂，不过咱们可以使用这个插件来解决这个尴尬问题，当然也可以使用外部网址解决，比如bejson这个网站~  





**8、Mybatis-log-plugin**

开发的项目一般都少不了日志系统，而我们在书写mysql语句的时候，参数的对应，往往有时候会忽略，mybatis自己控制的参数编译对应，个人感觉有点反人类，我们可以使用这个插件变成自己比较直观的对应~

选中需要转换的mybatis log日志，然后点击右键，选择Restore sql from slection



**9、Alibaba Java Coding Guidelines**

一款阿里巴巴公司试行的开发设计规范~ 



10. **彩虹颜色括号**：Rainbow Brackets



**11、阿里 p3c**

https://github.com/alibaba/p3c/blob/master/idea-plugin/README_cn.md



另外还有一些其他的插件：
阿里代码规约检测：Alibaba Java Coding Guidelines
自动生成序列图插件：SequenceDiagram
快捷键提示工具：Key promoter X
代码注解插件： Lombok
代码生成工具：CodeMaker
代码质量检查工具：SonarLint
单元测试测试生成工具：JUnitGenerator
Mybatis 工具：Free Mybatis plugin
JSON转领域对象工具：GsonFormat
字符串工具：String Manipulation
Redis可视化：Iedis
K8s工具：Kubernetes
