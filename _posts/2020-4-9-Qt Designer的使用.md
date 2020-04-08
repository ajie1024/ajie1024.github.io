---
layout:     post
title:      Qt Designer的使用--01 界面介绍
subtitle:   print的格式化输出
date:       2020-04-06
author:     Phoenix_W
header-img: img/QtDesigner01.jpg
catalog: true
tags:
    - python3
    - UI
    - PyQt5
    - Qt Designer
    - PyQt5教程（一）
    - PyQt5教程
---


## 前言

制作程序UI界面，一般可以通过UI制作工具和纯代码编写两种方式来实现，在PyQt5中，也可以采用这两种方式。接下里我将在blog中记录并讲解通过Qt Designer工具来制作UI界面


## 正文

### 1 Qt Designer快速入门

  Qt Designer，即Qt设计师，Qt Designer是PyQt程序UI界面的实现工具，Qt Designer工具使用简单，可以通过拖拽和点击完成复杂界面设计，并且设计完成
的.ui程序可以转换成.py文件供python程序调用。

  Qt Designer符合MVC（模型model - 视图view - 控制器Ctr)设计模式，做到了显示和业务逻辑的分离。
  Qt Designer具有以下优点：
+ 使用简单，通过拖拽和点击就可以完成复杂的界面设计，而且还可以随时预览查看效果图（快捷键：ctr+r)
+ 转换Python文件方便。Qt Designer可以将设计好的用户界面保存为.ui文件，其实是XML格式的文本文件。为了在PyQt中使用.ui文件，可以通过pyuic5命
  令将.ui文件转换为.py文件，然后将.py文件引入到自定义的Python代码中。
  Qt Designer默认安装在%/python.\*/site-pages/pyqt5-tools 目录下，在笔者的机器上Qt Designer的安装路径是D:\\WinPyQt5.9-32bit-3.5.3.1。
  Qt Designer的启动文件为Designer.exe, 如图1-1所示：

![1-1](https://raw.githubusercontent.com/phoenixwang1024/phoenixwang1024.github.io/master/img/QtDesigner/QtDesigner1-1.jpg)

### 1.1 新建主窗格

  在Qt Designer的安装路径下双击designer.exe文件，打开PyQt 5的Qt Designer， 会自动弹出“新建窗体”对话框， 如图 1-2所示。在模板选项中，最常用的就是Widget（通用窗口)和 Main Window （主窗口）。 在PyQt 5中 Widget被分离出来，用来替代 Dialog，并将 Widget 放入了 QtWiget模块库中。

![1-2](https://raw.githubusercontent.com/phoenixwang1024/phoenixwang1024.github.io/master/img/QtDesigner/QtDesigner1-2.jpg)

  模板选择“ Main Window”， 创建一个主窗口，保存并没命名firstMainWin.ui,如图1-3 所示， 主窗口默认添加了菜单栏、工具栏和状态栏。

![1-3](https://raw.githubusercontent.com/phoenixwang1024/phoenixwang1024.github.io/master/img/QtDesigner/QtDesigner1-3.jpg)

### 1.2 窗口主要区域介绍


  在图1-3 中标注了窗口的主要区域，区域 1 是 Widget Box（工具箱）， 如图1-4所示， 其中提供了很多控件，每个控件都有自己的名称，提供不同的功能， 比如常用的按钮、 单选钮、 文本框登， 可以直接拖放到主窗口中。 在菜单栏中选择“窗体” \-\- "预览"， 或者按"Ctr+R" 快捷键， 就可以看到窗口的预览效果了。

  ![1-4](https://raw.githubusercontent.com/phoenixwang1024/phoenixwang1024.github.io/master/img/QtDesigner/QtDesigner1-4.jpg)
![1-4](https://raw.githubusercontent.com/phoenixwang1024/phoenixwang1024.github.io/master/img/QtDesigner/QtDesigner1-5.jpg)
可以从 Buttons 栏拖拽一个按钮到主窗口（区域2）中， 如图 1-5 所示。

![1-5](https://raw.githubusercontent.com/phoenixwang1024/phoenixwang1024.github.io/master/img/QtDesigner/QtDesigner1-5.jpg)

在对象查看器（区域 3）中，可以查看主窗口中放置的对象列表，如图 1- 6所示。

![1-6](https://raw.githubusercontent.com/phoenixwang1024/phoenixwang1024.github.io/master/img/QtDesigner/QtDesigner1-6.jpg)

区域 4 是Qt Designer 的属性编辑器，其中提供了对窗口、控件、布局的属性编辑功能， 如图 1-7 所示。

![1-7](https://raw.githubusercontent.com/phoenixwang1024/phoenixwang1024.github.io/master/img/QtDesigner/QtDesigner1-7.jpg)


* <font color=#008B8B > objectName| 控件对象名称 </font>
* <font color=#008B8B >geometry | 相对坐标系</font>
* <font color=#008B8B >sizePolicy | 控件大小策略</font>
* <font color=#008B8B >minimumSize | 最小宽度、高度</font>
* <font color=#008B8B >maximumSize | 最大宽度、高度</font> 如果想让窗口或者控件大小固定，则可以将 minimumSize 和 maximumSize 这两个属性设置成一样的数值
* <font color=#008B8B >font | 字体</font>
* <font color=#008B8B >cursor | 光标</font>
* <font color=#008B8B >windowTitle | 窗口标题</font>
* <font color=#008B8B >windowsIcon/windowsIcon | 窗口图标/控件图标</font>

### ps

打包了教程所用的软件环境，不会影响到电脑本身环境，简单配置后即可运行教程中代码，适合新手和不想倒腾老鸟。

[软件包百度云下载 提取码：lvdn](https://pan.baidu.com/s/1bAy5hJ_4ea0nM7gpmJhjiQ)
