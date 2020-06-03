---
layout: post
title: 常用快捷键-Sublime
date: 2020-05-29 22:12:34
tags: 
 - 工具
---

### Sublime 快捷键

1. 设置
    •Ctrl + `： 打开Sublime Text控制台
    •Ctrl + K, Ctrl + B： 组合键，显示或隐藏侧栏
    •F11： 切换普通全屏
    •Shift + F11： 切换无干扰全屏

2. 编辑
    •Ctrl + Enter： 在当前行下面新增一行然后跳至该行
    •Ctrl + Shift + Enter： 在当前行上面增加一行并跳至该行
    •Ctrl + ←/→： 进行逐词移动，
    •Ctrl + Shift + ←/→： 进行逐词选择
    •Ctrl + ↑/↓: 移动当前显示区域（只是显示窗口的变化，文件不会被修改）
    •Ctrl + Shift + ↑/↓： 移动当前行（文件会被修改）

3. 选择
    •Ctrl + D： 选择当前光标所在的词并高亮该词所有出现的位置，再次Ctrl + D，会选择该词出现的下一个位置
    •Ctrl + K： 在多重选词的过程中，会将当前选中的词进行跳过
    •Ctrl + U： 在多重选词的过程中，进行回退，
    •Esc： 退出多重编辑
    •Ctrl + Shift + L： 将当前选中区域打散，然后进行同时编辑
    •Ctrl + J： 把当前选中区域合并为一行

4. 查找
    •对使用Shift + ←/→或Ctrl + D或鼠标选中的关键字进行搜索： •F3： 跳到关键字下一个出现位置
    •Shift + F3： 跳到关键字上一个出现位置
    •Alt + F3： 选中关键字出现的所有位置（之后可以进行快速替换）

•Ctrl + F： 调出搜索框 •Enter： 跳至关键字下一个位置
•Shift + Enter： 跳至关键字上一个位置
•Alt + Enter： 选中关键字出现的所有位置（同样的，接下来可以进行快速替换）

•Ctrl + H： 调出替换框进行替换 •Ctrl + Shift + H： 输入替换内容后，替换当前关键字
•Ctrl + Alt + Enter： 输入替换内容后，替换所有匹配关键字。(NOTE: 注意此时如果鼠标焦点在编辑窗口中，则替换失败，将鼠标焦点调到替换框中，Ctrl + Alt + Enter才会起作用)

•Ctrl + Shift + F： 开启多文件搜索&替换
•Alt + C： 切换大小写敏感（Case-sensitive）模式
•Alt + W： 切换整字匹配（Whole matching）模式
•Alt + R： 切换正则匹配模式的开启/关闭

5. 跳转
•Ctrl + P： •列出当前打开的文件（或者是当前文件夹的文件），输入文件名然后 Enter 跳转至该文件
•组合跳转（“Go To Anything”）：Ctrl + P匹配到文件后，我们可以进行后续输入以跳转到更精确的位置 •@ 符号跳转：输入@symbol跳转到symbol符号所在的位置
•# 关键字跳转：输入#keyword跳转到keyword所在的位置
•: 行号跳转：输入:12跳转到文件的第12行


•Ctrl + R：  •列出当前文件中的符号（例如类名和函数名，但无法深入到变量名），输入符号名称 Enter 即可以跳转到该处。
•会列出Markdown文件的大纲

•F12： 快速跳转到当前光标所在符号的定义处（Jump to Definition）。比如当前光标所在为一个函数调用，F12会跳转至该函数的定义处。
•Ctrl + G： 输入行号以跳转到指定行

6. 窗口和Tab页
•Ctrl + N： 在当前窗口创建一个新标签
•Ctrl + Shift + N： 创建一个新窗口（该快捷键 和搜狗输入法快捷键冲突）
•Ctrl + W： 关闭标签页，如果没有标签页了，则关闭该窗口
•Ctrl + Shift + T： 恢复刚刚关闭的标签。

7. 分屏
•Alt + Shift + 2： 进行左右分屏 
•Alt + Shift + 8进行上下分屏
•Alt + Shift + 5进行上下左右分屏（即分为四屏） 
•Ctrl + 数字键： 跳转到指定屏
•Ctrl + Shift + 数字键： 将当前屏移动到指定屏

8. 格式化
•Ctrl + [： 向左缩进
•Ctrl + ]： 向右缩进
•Ctrl + Shift + V： 可以以当前缩进粘贴代码
•Tab： 自动补全关键字

9. 括号
•Ctrl + M： 可以快速的在起始括号和结尾括号间切换
•Ctrl + Shift + M：可以快速选择括号间的内容
•Ctrl + Shift + J: 对于缩进型语言（例如Python）可以快速选择相同缩进语句块的内容

NOTE：

1. Ctrl + Shift + F： 开启多文件搜索&替换，此快捷键和搜狗输入法的简繁切换快捷键有冲突，所以当你调不出搜索框时，注意一下当前是否切换到了搜狗输入法，如果是的话，切换到英文输入法，然后再Ctrl + Shift + F调出。

2. Ctrl + Shift + F： 开启多文件搜索&替换, 默认在当前打开的文件和文件夹进行搜索/替换，



我们可以指定在当前打开的文件进行搜索/替换



2.4 设置

2.4.1 单用户设置

1. sublime Text 3的默认设置文件无法修改 （Preferences/Settings - Default）

2. 如果你想修改配置（比如字体等），需要修改User下的配置文件（Preferences/Settings - User），将如下代码copy进去【2】【3】


复制代码
{
    "color_scheme": "Packages/Color Scheme - Default/Monokai.tmTheme",
    // 设置Courier New等宽字体，以便阅读
    "font_face": "Courier New",
    "font_size": 12.0,
    // 使光标闪动更加柔和
    "caret_style": "phase",
    // 高亮当前行
    "highlight_line": true,
    // 高亮有修改的标签
    "highlight_modified_tabs": true,

    "ignored_packages":
    [
        "Vintage"
    ]
}

复制代码

NOTE： 所添加的设置要放在下面这段代码前面，否则会报错；如果将其放在该段代码段后面的话，要给中括号后面添加一个逗号。

    "ignored_packages":
    [
        "Vintage"
    ],

3. 如果想设置Tab键等代码规范，可以如下设置【2】


复制代码
    // 设置tab的大小为4
    "tab_size": 4,
    // 使用空格代替tab
    "translate_tabs_to_spaces": true,
    // 添加行宽标尺
    "rulers": [80, 100],
    // 显示空白字符
    "draw_white_space": "all",
    // 保存时自动去除行末空白
    "trim_trailing_white_space_on_save": true,
    // 保存时自动增加文件末尾换行
    "ensure_newline_at_eof_on_save": true, 

复制代码

2.4.2 修改sublime Text 的默认配置文件位置

1. 安装完sublime text，在第一次运行的时候，sublime text 会在%appdata%目录下生成一个Sublime Text 3的文件夹，用于存放配置文件，以及后面安装的各种插件。

2. 可以把这个文件移动到sublime text 3安装目录下，便于设置完后打包。以便同时在公司机器、家里机器上保障2者配置能同步。具体设置可参考【4】

2.4.3 主题与配色

1. How to install a Sublime Text theme？

有2种方法：

（1）可以使用Colorsublime plugin 来安装新的theme（the easy way）。

在Package Control搜索'Colorsublime'，然后install the plugin。安装步骤，参考【6】

安装步骤：

（2）手动安装（the hard way）。

参考【5】

2. 安装Colorsublime plugin

有2种办法：

（1）使用Package Control (recommended)

按下Ctrl+Shift+P调出命令面板，输入install 调出 Install Package 选项并回车，在列表中输入插件名Colorsublime，选择插件安装。

（2）手动安装

参考【6】

3. Colorsublime plugin用法

（1）Press ctl+shift+p to open up Sublime Text's command menu

（2）Select Colorsublime: Install Theme

（3）Use the arrow keys to run through the themes and see your current tab change in realtime!
