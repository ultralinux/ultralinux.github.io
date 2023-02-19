---
title: hexo持久化链接
abbrlink: 17e5a2b6
date: 2023-02-19 16:15:15
tags: blog.ultralinux.cn
categories: ultralinux_blog
description: 相较于跟随更新变化的URL更利于SEO,有一点点作用哦.我听说.html有利于SEO是真的吗,∑(〟OОO)真…真的吗!?
---

## 利用hexo-abbrlink插件实现链接持久化

GitHub [项目地址](https://github.com/rozbo/hexo-abbrlink)

```bash
npm install hexo-abbrlink --save
```

## 修改hexo框架配置文件 _config.yml文件

```yaml
permalink: archives/:abbrlink.html
```



## 添加相应的配置信息

```bash
# abbrlink config
abbrlink:
  alg: crc32      #支持crc16（默认）和crc32
  rep: hex        #支持dec（默认）和hex
  drafts: false   #（true）处理草稿，（false）不处理草稿。false（默认）
  # 从目录树生成类别
  # depth: 要生成的目录树的最大深度，应大于0
  auto_category:
     enable: true  #true(默认)
     depth:        #3(默认)
     over_write: false 
  auto_title: false #启用自动标题，可按路径自动填充标题
  auto_date: false #启用自动日期功能，可以按今天的时间自动填充日期
  force: false #启用强制模式，在此模式下，插件将忽略缓存，并为每个帖子计算abbrlink，即使它已经有了abbrlink。
```

## 重新渲染

```bash
$ hexo clean && hexo g
```

- hexo 持久化链接中出现 undefined 的问题

	- 在执行 hexo clean && hexo g 后莫名其妙的消失了神奇

	- 在此之前我是用的是 

		- hexo s ("server": "hexo clean && hexo generate && hexo server")

		- hexo d("deploy": "hexo clean && hexo generate && hexo deploy",)

		- hexo s会出现undefined 的问题

		- hexo d则是完全无效的，和之前一样没有任何变化

		- [我看到了这个，但还未来得及采用这个方案就好了]:https://www.fadai.cc/posts/fb8c11fe/

		- 貌似_好像,大概看到过 一片关于 什么延迟 什么的，忘记惹，算了，就当不存在的问题好伐QAQ


## 效果图

生成的链接如下所示:

[看看我嘻嘻 o(*////▽////*)q](https://blog.ultralinux.cn)

```html
crc16 & hex
https://post.zz173.com/posts/66c8.html

crc16 & dec
https://post.zz173.com/posts/65535.html
```

```html
crc32 & hex
https://post.zz173.com/posts/8ddf18fb.html

crc32 & dec
https://post.zz173.com/posts/1690090958.html
```

[蟹蟹٩('ω')و]:https://blog.cmyr.ltd/archives/d90e02c6.html





## ,,,

删除.deploy_git文件夹

删除public文件夹

hexo clean && hexo g && hexo d

Netlify_清除缓存并重试最新分支的提交

访问Netlify永久链接查看





cdn缓存更新奇慢:

1. 又拍云有问题,梅克金
2. Netlify有问题,默克金,性能拉胯

