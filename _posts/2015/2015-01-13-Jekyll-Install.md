---

title: Jekyll安装指南
layout: default
categories: [Jekyll]
tags: [Jekyll, Ruby, Gem]

---


### 安装Ruby Installer和DevKit

从如下地址下载RubyInstaller 2.1.5，64位版本，并安装到***D:\Ruby***

[rubyinstaller-2.1.5-x64.exe](http://dl.bintray.com/oneclick/rubyinstaller/rubyinstaller-2.1.5-x64.exe?direct "rubyinstaller-2.1.5-x64.exe")

同样网页下载64位Devkit：DevKit-mingw64-64-4.7.2-20130224-1432-sfx.exe，安装到***D:\Ruby\Devkit***，或CSDN上下载：

[DevKit-mingw64-64-4.7.2-20130224-1432-sfx.exe](http://dldx.csdn.net/fd.php?i=997369170814104&s=a5d7f1928ccd9fabc8dd3c9722c3ed77)

安装和配置：

    cd D:\Ruby\DevKit
    ruby dk.rb init
    ruby dk.rb install


### 安装Jekyll
修改gem源，先删除原来的源，增加taobao的源（*http://ruby.taobao.org*，直接用ip）


    gem sources -r http://rubygems.org/
    gem sources -a http://223.6.253.37/
    gem install jekyll
    gem install rdiscount
    gem install redcarpet


### 运行Jekyll

    jekyll new Blog
    cd Blog
    jekyll serve

打开，[http://localhost:4000/](http://localhost:4000/)，就可以看见网页了。