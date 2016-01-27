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
wget https://swift.org/builds/ubuntu1404/swift-2.2-SNAPSHOT-2015-12-18-a/swift-2.2-SNAPSHOT-2015-12-18-a-ubuntu14.04.tar.gz
```

```bash
tar -zxvf swift-2.2-SNAPSHOT-2015-12-18-a-ubuntu14.04.tar.gz
```
```bash
export PATH=/path/to/swift-2.2-SNAPSHOT-2015-12-18-a-ubuntu14.04/usr/bin/:"${PATH}"
```

2.如果你是全新的ubuntu环境，肯定少了很多support的包，运行如下Script

```bash
apt-get update
sudo apt-get install git cmake ninja-build clang uuid-dev libicu-dev icu-devtools libbsd-dev libedit-dev libxml2-dev libsqlite3-dev swig libpython-dev libncurses5-dev pkg-config
```

3.检查swift命令是否配置成功
```bash
swift --version
```

来个栗子：
```bash
print("Hello, Swift!")
41 + 1
import Glibc
random()
```
