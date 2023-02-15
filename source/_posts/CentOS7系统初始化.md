---
title: CentOS 7 系统初始化
date: 2022-04-04 10:01:36
tags:
categories: 未分类
description: 断片了
copyright_author: ultralinux
copyright_author_href: 不给看，嘿嘿！
copyright_url: https://blog.ultralinux.cn
copyright_info: 此文章版权归ultralinux所有，如有转载，请注明來自原作者
---

> 禁用防火墙与selinux


    iptables -F
    systemctl stop firewalld && systemctl disable firewalld
    setenforce 0
    sed -i 's/SELINUX=enforcing/SELINUX=disabled/g' /etc/selinux/config



> 系统源与第三方源


    wget -O /etc/yum.repos.d/CentOS-Base.repo  http://mirrors.aliyun.com/repo/Centos-7.repo
    wget -O /etc/yum.repos.d/epel.repo  http://mirrors.aliyun.com/repo/epel-7.repo
    yum clean all && yum makecache



> 安装常用工具


    yum install wget net-tools telnet tree nmap sysstat lrzsz dos2unix bind-utils -y



> 关闭swap


    swapoff -a
    sed -ri 's/.*swap.*/#&/' /etc/fstab



> 时间同步
