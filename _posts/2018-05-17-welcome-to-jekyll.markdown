---
layout: post
title:  "window7安装pip问题"
date:   2020-12-18 21:01:00 +0800
tags: python
color: rgb(135,206,250)
cover: 'http://qqpublic.qpic.cn/qq_public/0/0-2617900933-EB99ECDA523A42E46FC6A268DDD63A83/0?fmt=jpg&size=57&h=1244&w=700&ppv=1'
description: '这篇文章时windows7系统填坑安装pip的过程'
---



## windows7安装pip时遇到的一些问题填坑

​    安装python后，需要用pip安装一些库，这是安装pip的过程和中间遇到的一些问题

1. 首先去鼠标右键我的电脑  -> 属性 -> 高级系统设置 -> 环境变量 -> 编辑PATH -> 在最后面加上我们的Python安装路径 -> 点击确定

   ![image-20201208221412095](https://i.loli.net/2020/12/08/BuwgeqJ51R9foQp.png)

2. 再[点这去下载](https://pypi.org/project/pip/#files)下载pip的软件包，下载之后打开cmd，切换到pip下的文件目录里，运行”python setup.py install“，发现”No module name ‘setuptools’ “，（缺少‘setuptools’模块，所以无法安装，去下载个模块）

   ![image-20201208222307553](https://i.loli.net/2020/12/08/VB4jwQqhL7r1PWO.png)

3.点击[下载](https://pypi.io/packages/source/s/setuptools/setuptools-33.1.1.zip),下载之后，打开cmd，切换到这个解压包文件目录里面，运行”python setup.py install“，出现成功界面

![image-20201208222910642](https://i.loli.net/2020/12/08/1FtKsH7PGz5rdMT.png)

4.回到之前的pip安装目录，接着运行”python setup.py install“，又报错，此时出现这个问题”zip does not support time“。![image-20201208223458057](https://i.loli.net/2020/12/08/UpPK4DxaORq7j5t.png)

![image-20201208223026622](https://i.loli.net/2020/12/08/pM7zets3gv4L8yC.png)

5.我还以为安装成功了呢，以为只是一个小插件出的毛病，结果发现并没有安装上

![image-20201208223343688](https://i.loli.net/2020/12/08/Dwp9Oi4s8MGWovn.png)

6.在该pip文件目录下，输入命令” python -m ensurepip“，发现成功安装。又更新pip版本”python -m pip install --upgrade pip“也能成功运行![image-20201208223850233](https://i.loli.net/2020/12/08/esXYcfrI7x4B1SN.png)

![image-20201208223906074](https://i.loli.net/2020/12/08/rCbImKp2w35T8nM.png)

