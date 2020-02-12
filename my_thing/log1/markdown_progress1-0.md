     进阶语法

 一、更改字体、大小、颜色
    二、为文字添加背景色
    三、设置图片大小
        1、设置设置图片百分比
        2、设置图片大小
        3、设置图片居中
    参考链接

一、更改字体、大小、颜色

Markdown语法

<font face="黑体">我是黑体字</font>
<font face="微软雅黑">我是微软雅黑</font>
<font face="STCAIYUN">我是华文彩云</font>
<font color=red>我是红色</font>
<font color=#008000>我是绿色</font>
<font color=Blue>我是蓝色</font>
<font size=5>我是尺寸</font>
<font face="黑体" color=green size=5>我是黑体，绿色，尺寸为5</font>

    1
    2
    3
    4
    5
    6
    7
    8

效果如下：

我是黑体字
我是微软雅黑
我是华文彩云
我是红色
我是绿色
我是蓝色
我是尺寸
我是黑体，绿色，尺寸为5
二、为文字添加背景色

由于 style 标签和标签的 style 属性不被支持，所以这里只能是借助 table, tr, td 等表格标签的 bgcolor 属性来实现背景色。故这里对于文字背景色的设置，只是将那一整行看作一个表格，更改了那个格子的背景色（bgcolor）

Markdown语法

<table><tr><td bgcolor=yellow>背景色yellow</td></tr></table>

    1

效果如下
背景色yellow
三、设置图片大小
1、设置设置图片百分比

Markdown语法

<img src="http://pic11.photophoto.cn/20090626/0036036341009653_b.jpg" width="50%" height="50%">

    1

效果如下
2、设置图片大小

Markdown语法

<img src="http://pic11.photophoto.cn/20090626/0036036341009653_b.jpg" width="251" height="350" >

    1

效果如下
3、设置图片居中

Markdown语法

<div align=right><img src="http://pic11.photophoto.cn/20090626/0036036341009653_b.jpg" width="50%" height="50%"></div>

    1

效果如下

ps：center,left,left
参考链接

RGB颜色对照表

Markdown 语法大全 包括设置字体 颜色

Markdown: Basics （快速入门）

CSDN-markdown 文字样式设置（字体, 大小, 颜色, 高亮底色）

