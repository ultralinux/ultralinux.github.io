---
title: VMware Workstation Pro 16
date: 2022-04-04 12:10:58
tags:
categories: 未分类
description: 关于win个人喜欢的一些软件
copyright_author: ultralinux
copyright_author_href: 不给看，嘿嘿！
copyright_url: https://blog.ultralinux.cn
copyright_info: 此文章版权归ultralinux所有，如有转载，请注明來自原作者
---

*   [官方下载位置](https://www.vmware.com/products/workstation-pro/workstation-pro-evaluation.html)
~~*   [ul度盘](https://pan.baidu.com/s/1OjC1UhsftYUqstsmPSDhCA?pwd=ulcn)提取码：ulcn~~
## 安装建议：

一首下一步即可，关闭自动检查更新
![](https://img.ultralinux.cn/img/202302151238318.png?imageslim)
![](https://img.ultralinux.cn/img/202302151238981.png?imageslim)
![](https://img.ultralinux.cn/img/202302151238705.png?imageslim)

修改网段。如有需要，关闭DHCP服务（禁止自动分配ip）
![](https://img.ultralinux.cn/img/202302151238958.png?imageslim)
![](https://img.ultralinux.cn/img/202302151238748.png?imageslim)
![这里的192.168.100.1，（所在网段）点1的IP地址是无法使用的因为在安装VMware时自动生成的VMnet8虚拟网卡IP地址默认为100.1用于宿主机与虚拟机通信使用（所修改网段的点1）IP地址，并且当修改为其他网段时VMnet8虚拟网卡的IP地址也会自动修改为相应网段的点1IP地址。](https://img.ultralinux.cn/img/202302151238245.png?imageslim)
![若想使用相应网段点1IP地址为网关需要在宿主机VMnet8修改为其他同网段不使用的IP地址，这样就可以使用192.168.100.1（相应网段的.1IP地址）注意，当修改VMnet虚拟网卡网段时宿主机的VMnet8IP地址还会自动修改为相应IP的点1IP地址，再次修改即可](https://img.ultralinux.cn/img/202302151238786.png?imageslim)

当然也可以以创建多个虚拟网卡并选择需要的模式--桥接模式、仅主机模式、NAT模式。

