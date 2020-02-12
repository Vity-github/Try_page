![img](https:////upload-images.jianshu.io/upload_images/1244049-116951fe16c2b87e.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200)



# 利用github部署自己的个人网页





本篇记录了如何通过GitHub Page发布个人网页，所以适合以下设计师阅读：

1. 有一定前端知识；
2. 想在网页上显示点什么又不想麻烦去折腾域名和服务器；
3. 有Mac电脑，我还没研究Windows。

相关文章有很多，官网也写得很详细，我写得有点啰嗦了，因为是第一篇关于GitHub的文章所以尽量介绍详细点，避免日后查。之后还会写一篇用GitHub搭建静态博客，也就是CMS(内容管理系统)的文章。

以下正文：

------

## 1.起源

最早学习前端的时候就写过一些页面，也想自己部署到服务器上，但是又不想折腾域名和服务器（域名要购买还要备案，服务器也需要购买）。所以一直没有做这件事，准备简历的时候放的也是本地的代码。

直到前两天，因为公司官网下线无法访问（公司官网是我写的一个静态页面），所以才想是否还有别的方式可以展示，于是找到这么个神器GitHub Page。GitHub都不陌生，毕竟~~全球最大男性交友网站~~世界上最大的代码存放网站和开源社区[1](https://zh.wikipedia.org/wiki/GitHub)。它旗下GitHub Page更是可以免费托管你的静态页面，虽说空间不限，但据说体积要控制在1G以下[2](https://www.zhihu.com/question/21282780)。

折腾了半天总算是成功发布了页面，[官方文档](https://pages.github.com/)介绍得也非常详细，以下是我操作过后的具体步骤。

## 2.注册GitHub账号

注册地址：https://github.com/join?source=login

自行注册。

## 3.创建Git仓库（Repository）

点击右上角的加号创建仓库

![img](https:////upload-images.jianshu.io/upload_images/1244049-cac600d3196ca6b6.png?imageMogr2/auto-orient/strip|imageView2/2/w/782)

填写仓库名称就可以点击下面的绿色按钮创建了。

其中：

- Description——仓库描述，选填；
- Public，Private——GitHub限制免费用户只能创建公开仓库；
- Initialize this repository with a README——初始化仓库时添加README，readme是一个说明文件，用markdown语法编写，打上勾的话就默认添加了这个文件，如果不打勾后期也可以自己添加；

![img](https:////upload-images.jianshu.io/upload_images/1244049-617ee90efd948337.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200)

## 3.本地配置Git

创建好仓库后显示下图页面，点击红框标记按钮复制仓库地址。

![img](https:////upload-images.jianshu.io/upload_images/1244049-8c8d8aa311cad45d.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200)

这时候需要用到Git命令了 ，Git是一个分布式版本控制软件[3](https://zh.wikipedia.org/wiki/Git)，我们就通过Git命令来同步和管理代码。

Git的安装参考这篇文章：[安装Git](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/00137396287703354d8c6c01c904c7d9ff056ae23da865a000)

安装好之后初次运行Git需要做一些配置：

1. 打开系统自带的Terminal；

   ![img](https:////upload-images.jianshu.io/upload_images/1244049-5e8df46f16e5fbbc.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200)

1. 设置username和email，github每次commit（提交代码）都会记录他们，在Terminal中分别输入以下代码；

