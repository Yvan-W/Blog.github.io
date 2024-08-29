---
layout: '[layout]'
title: Ubuntu Server修改主机名和用户名(摸鱼篇)
date: 2024-03-09 16:52:09
category:
    - 教程
tags:
    - Ubuntu_Server
    - Linux 系统
cover: https://img.yvan.eu.org/mt/2024/07/25/66a21dfb28456.png
comments: true
---


- # 主机名
  <b><font size=3 face="宋体">
  > 主机名很简单,只需要更改hostname 和 hosts 即可
  > 首先输入下面命令,来查看现在的用户名
```bash
	hostname
```
  > 之后分别输入下面命令,来修改你想要的用户名
```bash
	sudo vi /etc/hostname
	sudo vi /etc/hosts
```
  > 重启
  </font></b>
- # 用户名
  <b><font size=3 face="宋体">
  > <font size=4 face="黑体">***用户名比较复杂,请认真阅读*** </font>

  > <font size=4 face="黑体" color=red>一定换到root用户下进行修改，普通用户下修改用户名后，执行sudo命令会提示密码错误。</font>

  ```bash
	sudo su
  ```
  > 可以使用sed命令进行批量修改
  > 1）修改passwd文件
  > 将passwd中原用户名修改成新用户名：
  ```bash
	vi /etc/passwd
  ```
  > 或者使用如下命令修改： 
  ```bash
	sed -i "s/\b旧用户名\b/新用户名/g" `grep 旧用户名 -rl /etc/passwd` 
  ```
  >  2）修改shadow文件
  > 将shadow中原用户名修改成新用户名：
  ```bash
	vi /etc/shadow
  ```
  > 或者用如下命令修改：
  ```bash
	sed -i "s/\b旧用户名\b/新用户名/g" `grep 旧用户名 -rl /etc/shadow`
  ```
  > 3）修改home目录下文件夹名
  > 将home目录下用户文件夹名修改为新用户的名：
  ```bash
	mv /home/旧用户名/ /home/新用户名
  ```

  > 4）修改sudo权限
  > 修改group文件，将原来的用户名替换成新用户名。
  ```bash
	vi /etc/group
  ```
  > 或者用如下命令修改：
  ```bash
	sed -i "s/\b旧用户名\b/新用户名/g" `grep 旧用户名 -rl /etc/group`
  ```
  </font></b>
- # 最后重启机器