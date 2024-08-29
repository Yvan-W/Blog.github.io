---
layout: '[layout]'
title: 物理机安装Ubuntu Server教程
date: 2024-03-09 16:52:09
category:
    - 教程
tags:
    - Ubuntu_Server
    - Linux 系统
cover: https://img.yvan.eu.org/mt/2024/07/14/6693e0ac959b5.jpg
comments: true
---

- # 安装前准备
    <b><font size=3 face="宋体">
    > 首先，我们要准备一个可以作为安装介质的空U盘（建议8G以上），可以利用网上的一些工具来制作安装介质，本人这里推荐Ventoy  [下载链接](https://github.com/ventoy/Ventoy/releases/latest)  
    > [![Ventoy](https://img.yvan.cn.eu.org/file/0985585d83ecedcda5cd1.png)](https://img.yvan.cn.eu.org/file/0985585d83ecedcda5cd1.png)  
    > 下载对应文件，我这里是Windows 所以选Windows字样的文件，下载完后进行解压，运行  
- > <b><font size=3 face="黑体">请注意：U盘有数据的一定要***备份***！！！</font></b>

    > [![介质安装](https://img.yvan.cn.eu.org/file/37ccea7b1e697ce39e58f.png)](https://img.yvan.cn.eu.org/file/37ccea7b1e697ce39e58f.png)  
    > 运行后如上图，因为我这里已经安装过了，所以我点升级。  
    > [下载镜像](https://cn.ubuntu.com/download/server/step1) 并拷贝到U盘中（自行确认自己的平台构架！！！）
    > 到这里，准备工作就完成了  
    </font></b>
- # 开始安装
    <b><font size=3 face="宋体">
    > 我们拔掉电源（也就是要在关机状态下），连接好你的设备，由于我在学校，没有显示器，只能靠USB视频采集器来操作  
    > [![连接设备](https://img.yvan.cn.eu.org/file/f77673fddae7d71479cde.jpg)](https://img.yvan.cn.eu.org/file/f77673fddae7d71479cde.jpg)  
    > 好，现在我们开机，我的设备是连续点按F8，自己的设备自己去百度，进入如下图选择Ubuntu镜像，然后选第一个选项
    > [![Ventoy界面](https://img.yvan.cn.eu.org/file/1aaf1e80ceb2c8680900d.png)](https://img.yvan.cn.eu.org/file/1aaf1e80ceb2c8680900d.png)  
    > 然后进入到如下界面，再次选第一个 Try or install Ubuntu Server，然后便会进入到安装导向界面，请慢慢等待  
    > [![选择2](https://img.yvan.cn.eu.org/file/4e1a4d544d628003a8938.png)](https://img.yvan.cn.eu.org/file/4e1a4d544d628003a8938.png)  
    > 等待过后，进入到如下界面,默认English即可.  
    > [![导向1](https://img.yvan.cn.eu.org/file/294ef716bef57d8f0c5ae.png)](https://img.yvan.cn.eu.org/file/294ef716bef57d8f0c5ae.png)  
    > 下几个界面亦可默认,如果有别的需求,自己百度改,直到进入这个界面  
    > [![导向2](https://img.yvan.cn.eu.org/api/file/30e456fd62ab3cc30dc6f.png)](https://img.yvan.cn.eu.org/api/file/30e456fd62ab3cc30dc6f.png)  
    > 至此,如果你没有配置网络环境的需求,请跳过(一般情况不需要配置,因为大部分是插的网线,直接自动配置),这里我就以无线为例,如图  
    > [![导向3](https://img.yvan.cn.eu.org/api/file/cbafa847e162d18ec744f.png)](https://img.yvan.cn.eu.org/api/file/cbafa847e162d18ec744f.png)  
    > [![导向4](https://img.yvan.cn.eu.org/api/file/b0788732a36b6248ad7a3.png)](https://img.yvan.cn.eu.org/api/file/b0788732a36b6248ad7a3.png)  
    > 此界面填写自己的网络信息,或者直接扫描WiFi  
    > [![导向5](https://img.yvan.cn.eu.org/api/file/3daefabe896ad8e7dad2d.png)](https://img.yvan.cn.eu.org/api/file/3daefabe896ad8e7dad2d.png)  
    > 如果需要静态IP,请自行配置,如图  
    > [![导向6](https://img.yvan.cn.eu.org/api/file/107d514d0e2457bef2053.png)](https://img.yvan.cn.eu.org/api/file/107d514d0e2457bef2053.png)  
    > [![导向7](https://img.yvan.cn.eu.org/api/file/845b97949e1873191d04b.png)](https://img.yvan.cn.eu.org/api/file/845b97949e1873191d04b.png)  
    > [![导向8](https://img.yvan.cn.eu.org/api/file/01307a5e0b529d3975739.png)](https://img.yvan.cn.eu.org/api/file/01307a5e0b529d3975739.png)  
    > 信息自己填写,不认识单词自己翻译
    > 我这样就算是连接成功
    > [![导向9](https://img.yvan.cn.eu.org/api/file/22ccf00b03e95fe2651f9.png)](https://img.yvan.cn.eu.org/api/file/22ccf00b03e95fe2651f9.png)
    > 连接完成后进行下一步,代理地址自行决定,对于软件源,想稳定就改成阿里云的,我这里放了一个清华源的,自行选择
```
    https://mirrors.tuna.tsinghua.edu.cn/ubuntu
```
    > 然后我们进行到下一步,磁盘配置  
    > 你可以选择默认配置,这里我是自定义的  
    > [![磁盘1](https://img.yvan.cn.eu.org/api/file/737cb2beb82f21e647a02.png)](https://img.yvan.cn.eu.org/api/file/737cb2beb82f21e647a02.png)  
    > [![磁盘2](https://img.yvan.cn.eu.org/api/file/55b359cadb9b2455cdf60.png)](https://img.yvan.cn.eu.org/api/file/55b359cadb9b2455cdf60.png)  
    > 最后 Done 并Continue  
    > [![磁盘3](https://img.yvan.cn.eu.org/api/file/7be683fd28411b13d71a4.png)](https://img.yvan.cn.eu.org/api/file/7be683fd28411b13d71a4.png)  
    <b><font size=5 face="黑体">***对于上面的volume group ，这里建议关闭哦~~*** </font></b>
    > 下一步则是填写信息一类的,自行填写剩下的全部默认,其中有一项 你要安装openssh server 除非你不想通过局域网连接主机
    </font></b>
- # *到这里,安装过程便结束了,剩下的静静等待安装完成,最后手动重启*