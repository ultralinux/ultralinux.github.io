---
title: 最小化安装CentOS7.9
date: 2022-04-04 10:53:36
tags:
categories: 未分类
description: 最后的Centos
copyright_author: ultralinux
copyright_author_href: 不给看，嘿嘿！
copyright_url: https://blog.ultralinux.cn
copyright_info: 此文章版权归ultralinux所有，如有转载，请注明來自原作者
---


## 壹、方向键上下选择直接安装，回车
![](https://img.ultralinux.cn/img/202302151055728.png?imageslim)

## 贰、等待到安装界面，选择系统语言
![](https://img.ultralinux.cn/img/202302151058398.png?imageslim)

## 叁、
![](https://img.ultralinux.cn/img/202302151100408.png?imageslim)
![](https://img.ultralinux.cn/img/202302151100695.png?imageslim)
![](https://img.ultralinux.cn/img/202302151100728.png?imageslim)

## 肆、建议手动分区
*   创建boot分区，/boot分区大小为1024M,文件系统类为xfs；


boot分区：是引导分区，作用：系统启动，在boot分区存着grub，内核文件等，centos7或8应该给1024M,考虑到后期yum update更新系统时有足够的空间存新的内核；在centos5或6上，boot分区给200M即可。



*   创建swap分区，swap分区最小为2G，文件系统类型为swap；


swap交换分区：swap分区通常被称为交换分区，这是一块特殊的硬盘空间，即当实际内存不够用的时候，操作系统会从内存中取出一部分暂时不用的数据，放在交换分区中，从而为当前运行的程序腾出足够的内存空间。一般swap分区为物理内存的1.5~2倍，当物理机内存多于16G后，swap分区给8~16G都可以。如果系统使用到了swap分区，建议添加物理内存或排查一下系统上是否有非法程序。



*   创建/根分区，/根分区50G,文件类型为xfs；


/根分区所有文件的逻辑存储位置，绝对路径的开始标志。
![](https://img.ultralinux.cn/img/202302151104839.png?imageslim)
![](https://img.ultralinux.cn/img/202302151104384.png?imageslim)
![](https://img.ultralinux.cn/img/202302151104816.png?imageslim)

## 伍、设置root管理员密码，完成配置。
![](https://img.ultralinux.cn/img/202302151104871.png?imageslim)
![](https://img.ultralinux.cn/img/202302151104780.png?imageslim)
