---
title: Xshell操作
categories: 未分类
description: xshell
copyright_author: ultralinux
copyright_author_href: 不给看，嘿嘿！
copyright_url: 'https://blog.ultralinux.cn'
copyright_info: 此文章版权归ultralinux所有，如有转载，请注明來自原作者
abbrlink: 7645713a
date: 2022-04-04 14:15:58
tags:
---
**一、图形化配置网络，关于配置VM的用处不大（也有其它方法）**
		1. 这里不建议使用DHCP获取IP地址(上我的船一个net8上网和xshell全都要)![在这里插入图片描述](https://img-blog.csdnimg.cn/20200503221713737.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)
		2. 这里设置网关，虚拟机网关就是这个偶，不要忘了DNS服务器![在这里插入图片描述](https://img-blog.csdnimg.cn/20200503222146494.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)
		3. 登录系统，图形化配置网卡（当然字符配置没什么不好的，我扩展一下）![在这里插入图片描述](https://img-blog.csdnimg.cn/20200503222857765.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)
		4. 这里可以修改主机名（看需求，可以不改）![在这里插入图片描述](https://img-blog.csdnimg.cn/2020050322311263.png)
		5. 配置IP地址（IP v4），使用Tab建或方向键选择、空格更改![在这里插入图片描述](https://img-blog.csdnimg.cn/2020050322440853.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)
		6. DNS服务器其他的也可以，网关是刚才自己配制NAT的网关
 [选择第二个编辑](https://img-blog.csdnimg.cn/20200503230252219.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200503234508118.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)
		7. 查看，需要联网，[真机的VM net8网卡配置](https://img-blog.csdnimg.cn/20200504113252665.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200503234920938.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)
**二、ssh远程控制——xshell**
			 1. 第一次打开提示用户数据位置![在这里插入图片描述](https://img-blog.csdnimg.cn/20200504113356462.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)
			 2. 新建会话，[也可先建一个文件夹](https://img-blog.csdnimg.cn/20200504113721349.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)![在这里插入图片描述](https://img-blog.csdnimg.cn/20200504113521101.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)
			 3. ![在这里插入图片描述](https://img-blog.csdnimg.cn/20200504114232234.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)![在这里插入图片描述](https://img-blog.csdnimg.cn/20200504114301654.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)
			 4. 模拟，为了方便记住密码![在这里插入图片描述](https://img-blog.csdnimg.cn/20200504114313162.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)![在这里插入图片描述](https://img-blog.csdnimg.cn/20200504114322422.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)		
**三、xshell**
 1. 设置当前会话，不建议设置默认的，[你可以复制会话](https://img-blog.csdnimg.cn/20200507180240592.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)
（对已创建的不生效）![在这里插入图片描述](https://img-blog.csdnimg.cn/20200504130237456.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)
 2. 可以查看更多的历史命令不好吗？![在这里插入图片描述](https://img-blog.csdnimg.cn/20200507164659750.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)
 3. 选择自己喜欢（不，效率和舒服我们全都要）![在这里插入图片描述](https://img-blog.csdnimg.cn/20200507164846322.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)
 4. 开启日志（回顾时再写实验也不晚，忘了截图哦）

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200504130549737.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)

 5. 查看的时候感觉不舒服（推荐一个软，，，）

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200507165703614.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)

 6. 方便的使用rz上传时，不要忘了sz

```bash
[root@localhost ~]# rz
-bash: rz: command not found
```
不小心翻船了，，，，

 1. 下载工具软件：lrzsz，安装方法：
```bash
 [root@localhost ~]# yum install lrzsz -y
```
**告诉你个小秘密：不要勾上下图的“发送文件到ASCII”哦，上船后会用不了的。**
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200507171653391.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)
[可以关闭这个提示，毕竟开心辣么重要](https://img-blog.csdnimg.cn/20200507171858877.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)
成功上船的小伙伴，如下图
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200507172005506.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)
 2. 下载，（也可以直接拖拽到会话上传）
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200507181144609.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200507181454643.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0ZsYWcyOTIw,size_16,color_FFFFFF,t_70)




