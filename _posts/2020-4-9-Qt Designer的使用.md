---
layout:     post
title:      Qt Designer的使用--01
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
---


## 前言

制作程序UI界面，一般可以通过UI制作工具和纯代码编写两种方式来实现，在PyQt5中，也可以采用这两种方式。接下里我将在blog中记录并讲解通过Qt Designer工具来制作UI界面


## 正文

### 1 Qt Designer快速入门

  Qt Designer，即Qt设计师，Qt Designer是PyQt程序UI界面的实现工具，Qt Designer工具使用简单，可以通过拖拽和点击完成复杂界面设计，并且设计完成
的.ui程序可以转换成.py文件供python程序调用。

  Qt Designer符合MVC（模型model - 视图view - 控制器Ctr)设计模式，做到了显示和业务逻辑的分离。
  Qt Designer具有以下优点：
    - 使用简单，通过拖拽和点击就可以完成复杂的界面设计，而且还可以随时预览查看效果图（快捷键：ctr+r)
    - 转换Python文件方便。Qt Designer可以将设计好的用户界面保存为.ui文件，其实是XML格式的文本文件。为了在PyQt中使用.ui文件，可以通过pyuic5命
      令将.ui文件转换为.py文件，然后将.py文件引入到自定义的Python代码中。
  Qt Designer默认安装在%/python.\*/site-pages/pyqt5-tools 目录下，在笔者的机器上Qt Designer的安装路径是D:\\WinPyQt5.9-32bit-3.5.3.1。
  Qt Designer的启动文件为Designer.exe, 如图1-1所示：
![1-1](https://phoenixwang1024.github.io/img/QtDesiner1-1.jpg)

### 1.1 新建主窗格

  在Qt Designer的安装路径下双击designer.exe文件，打开PyQt 5的Qt Designer， 会自动弹出“新建窗体”对话框， 如图 1-2所示。在模板选项中，最常用的就是Widget（通用窗口)和 Main Window （主窗口）。 在PyQt 5中 Widget被分离出来，用来替代 Dialog，并将 Widget 放入了 QtWiget模块库中。
![1-2](https://phoenixwang1024.github.io/img/QtDesiner1-2.jpg)


## ps：
希望这个能给大家提供帮助~
