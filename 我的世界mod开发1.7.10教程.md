# **我的世界mod开发1.7.10教程**

## 目录

- [我们先来了解一下我的世界1.7.10版本](###我们先来了解一下我的世界1.7.10版本)
- [mod开发的前置——配置工作环境](###mod开发的前置——配置工作环境)
- 

### **我们先来了解一下我的世界1.7.10版本**

1.7.10是一个mod众多，玩法比较全面的一个mc版本，而且这个版本有着比较稳定的mod服务器端，所以想要面向广大mc玩家开发mod的话，这个版本是个不错的选择。毕竟是mod的黄金时代

### **mod开发的前置——配置工作环境**

**目录**

- [构建forge](####构建forge)
- [下载idea](####接下来去下载idea吧)
- [安装一些idea的插件](####这个时候我们要安装一些idea的插件)

~~悄悄告诉你们，有想法的萌新大部分都死在这了QwQ~~

forge为开发者们提供了开发mod的平台，但是由于Gradle的资源都在国外，所以导致了构建forge极其漫长（我都构建了5个小时了←_←）

而且各种构建存在的问题导致有想法的萌新们一脸蒙逼，就比如：

![img](https://i0.hdslb.com/bfs/article/3508115fd96d58e0e048f73e96504c6a388db730.png)

​																									1.下载卡住



![img](https://i0.hdslb.com/bfs/article/ea3d5563131867864416a4210992780bc6c23f35.png)

​																								2.Java版本问题



![img](https://i0.hdslb.com/bfs/article/f927ac4f2ae0cb284904c4354f71130e62ef09de.jpg)

​																						3.改了Java环境变量



![img](https://i0.hdslb.com/bfs/article/749babbb30a3ba9048e847a3f60c9df8c393f684.png)

​																								4.开始卡住



![img](https://i0.hdslb.com/bfs/article/b4451d6383c82575f1d23cbb43bce7c1beb8ced1.png)																									
5.下载失败

看吧，你是不是也在这里面（提前真实）（你不在啊，那发给我QAQ）

解决方法：

1. 关掉重新加载，再卡住再关，再卡住......那你还是用手机开热点吧（这样 凉 快多了，切网络的时候会掉数据包，所以切网络之后要重新打开）
2. 换Java（把你的全部Java统统删掉），用Java8，这是个64位的：https://www.fixdown.com/down/55/2945/0（随便找的，虽然可能不能用，但好过你们找不到QwQ）
3. Java全删（把你的全部Java统统删掉），然后重下。链接同上（简单暴力，还不会出现各种问题）
4. 这。。。等呗QwQ
5. 重下重下再重下，不行就用方法1

#### 构建forge

~~好了，上面的1、5点其实是废话~~

**为了你们不出现各种各样的奇怪问题，也为了你们的不会死在第一步，所以我选择直接分享完成构建的构建包QwQ**

加**Q群**下载（实在是找不到有什么能提供存储的地方了）：**483315828**

**下载完之后把它解压到对应文件夹，打开forge-1.7.10-10.13.4.1614-1.7.10-src，就像这样：**

![img](https://i0.hdslb.com/bfs/article/88fb0167be8bfad2f4aefa11698e282a9cf3e0da.png)
打开forge-1.7.10-10.13.4.1614-1.7.10-src

**然后shift+右键文件夹里面的任意空位：**

![img](https://i0.hdslb.com/bfs/article/bc5f6c3ae92803358982a2fa07904744ce9d158f.jpg)
在forge-1.7.10-10.13.4.1614-1.7.10-src中打开cmd

**然后在cmd里面输入下面指令（显示BUILD SUCCESSFUL之后就下一条） ：**

gradlew.bat setupDecompWorkspace

构建工作环境

gradlew.bat build

构建工程

——————————————————————————————————————————————————

**好了，隔开一下QwQ，下面前两条几乎用不上，因为idea里面已经包含了这个操作了**

gradlew.bat runClient

运行客户端

gradlew.bat runServer

运行服务器

**所以直接到这来（在上面所打开的cmd中输入下面的）**

gradlew.bat idea

构建idea关联

#### **接下来去下载idea吧**

https://www.jetbrains.com/idea/

![img](https://i0.hdslb.com/bfs/article/7290fac09c505be7aceb1102729b747c493d59d4.png)
idea免费版

剩下的。。。阿巴阿巴阿巴阿巴（不想写了，淦）

**安装的时候把64位和.java勾了就好**

**安装完成之后先不要打开idea，回到这个目录：**

![img](https://i0.hdslb.com/bfs/article/5e48cfe22325bafe4828171dab2bb83127fa86c9.png)
打开巴拉巴拉巴拉.ipr

**双击打开这个文件，选择用idea运行，然后就可以看到这个亚子：**

![img](https://i0.hdslb.com/bfs/article/37f5d3eacd4c64295feb21dc8d19dd97f1e01f9a.png)
idea

**然后点右上角那个锤子看看能不能正常运行就ok了~~**

啊？你是想说为啥你不是中文的吗QwQ

##### **这个时候我们要安装一些idea的插件**

在idea左上角打开-文件-设置-选择“插件”项-搜索

Chinese (Simplified) Language Pack EAP

中文包↑
**Translation**

翻译插件↑



![img](https://i0.hdslb.com/bfs/article/bf02e77a9958b962ae9528a12a494bbb26292d71.png)
Chinese (Simplified) Language Pack EAP



![img](https://i0.hdslb.com/bfs/article/fcb6b2d542907b2b668e8c2e41f8a77c0bb20363.png)
Translation

好了~~回到上面所示的idea界面

点击左下角的终端，然后输入下面指令：

gradlew.bat genIntellijRuns

在idea中构建mc客户端启动和服务器启动

然后点一下右上角的三角形（那个锤子的旁边的旁边那个）

如果能正常启动mc的话那就ok了~~~
