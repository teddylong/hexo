---
title: 在Ubuntu中用ATOM来学习Swift
date: 2016-01-27 17:51:53
tags:
categories: 代码
---

最近很流行ATOM，，而且这半年一直在折腾Ubuntu，所以想用atom学学最新的Swift2.0，写写小例子：）

atom流行的原因在于有很多的插件，恩，确实很多！所以有什么新奇的想法，不妨往atom这边想想。。。。不过再怎么说，也是因为swift开源了，要么也不会在ubuntu上可以搞！

1.下载swift的ubuntu并设置好环境变量 （14.04）

```bash
$ wget https://swift.org/builds/ubuntu1404/swift-2.2-SNAPSHOT-2015-12-18-a/swift-2.2-SNAPSHOT-2015-12-18-a-ubuntu14.04.tar.gz
```

```bash
$ tar -zxvf swift-2.2-SNAPSHOT-2015-12-18-a-ubuntu14.04.tar.gz
```
```bash
$ export PATH=/path/to/swift-2.2-SNAPSHOT-2015-12-18-a-ubuntu14.04/usr/bin/:"${PATH}"
```
<!--more-->
2.如果你是全新的ubuntu环境，肯定少了很多support的包，运行如下Script

```bash
$ apt-get update
$ sudo apt-get install git cmake ninja-build clang uuid-dev libicu-dev icu-devtools libbsd-dev libedit-dev libxml2-dev libsqlite3-dev swig libpython-dev libncurses5-dev pkg-config
```

3.检查swift命令是否配置成功
```bash
$ swift --version
```

来个栗子：
```bash
print("Hello, Swift!")
41 + 1
import Glibc
random()
```

4.下载ATOM的swift支持组件，swift-debugger 和 language-swift
如果装好了ATOM，则可以运行如下命令：
```shell
$ apm install swift-debugger language-swift
```

5.现在就可以创建新的swift项目啦
```bash
$ mkdir MySwiftProject && touch MySwiftProject/main.swift && touch MySwiftProject/Package.swift
```
然后用atom命令打开这个文件夹
```bash
$ atom MySwiftProject
```
可以看到刚才生成的2个文件，一个是主文件main.swift和一个配置文件Package.swift。
然后给这个package一个name。把以下代码放在Package.swift中并保存。
```swift
import PackageDescription  
let package = Package(  
    name: "MySwiftProject"
  )
```
打开main.swift写点hello world吧：
```swift
let helloString = "Hello, World!"  
print(helloString)
```

按下alt-r来激活swift-debugger package。你会看到这样的界面：
![](http://7xqfs2.com1.z0.glb.clouddn.com/asdasdasdasd.png)

其中我们要填写的在输入框里面的就是图中写有「po foo」的地方

e=MySwiftProject (按回车)  
p=YourSwiftBinFolder (按回车)

这时 debugger 就会分别输出"swift path set"和"executable path set"了。可以开始愉快的玩耍啦！！！
