---
title: Rust_1.入门指南
date: 2022-12-06 13:59:07
tags: "Rust Language"
categories: Rust程序设计语言
description: 一个编程语言
copyright_author: ultralinux
copyright_author_href: 不给看，嘿嘿！
copyright_url: https://blog.ultralinux.cn
copyright_info: 此文章版权归ultralinux所有，如有转载，请注明來自原作者
---
> 官网

  [	Rust官网地址 ](https://www.rust-lang.org/)
[《Rust 程序设计语言》_非官方翻译](https://kaisery.github.io/trpl-zh-cn/)

[用户论坛](https://users.rust-lang.org/)
[stack overflow](https://stackoverflow.com/questions/tagged/rust)
[Rust官方 Discord](https://discord.com/invite/rust-lang)

```rust
rustc --version		//查看rust版本号
rustc x.y.z (abcabcabc yyyy-mm-dd)	//最新稳定版本的版本号、对应的 Commit Hash 和 Commit 日期
rustup update	//更新rust至最新版
rustup self uninstall	//卸载rust
rustup doc	//在浏览器查看本地文档
```
Rust 团队一直致力于借助 rust-analyzer 提供强大的 IDE 支持。详见[附录 D](https://kaisery.github.io/trpl-zh-cn/appendix-04-useful-development-tools.html)。
命名习惯为 hello_world.rs，而不是 helloworld.rs。

## 1.安装

 - Linux

```bash
ultralinux@ultralinux-PC:~/Desktop$ curl --proto '=https' --tlsv1.3 https://sh.rustup.rs -sSf | sh
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/215b464303564e10a152e6bbaa59c465.png)![在这里插入图片描述](https://img-blog.csdnimg.cn/3bd6b3d7e2b24cca9dea92c7276f5314.png)

```bash
ultralinux@ultralinux-PC:~/Desktop$ rustc --version
rustc 1.63.0 (4b91a6ea7 2022-08-08)
# 最新稳定版本的版本号、对应的 Commit Hash 和 Commit 日期

ultralinux@ultralinux-PC:~/Desktop$ echo $PATH
/home/ultralinux/.cargo/bin:/usr/local/bin:/usr/bin:/bin:/usr/local/games:/usr/games:/sbin:/usr/sbin
```

 - Windows

[链接](https://www.rust-lang.org/tools/install)
![在这里插入图片描述](https://img-blog.csdnimg.cn/aa919b87ca4c4a048c6e7b480925e304.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/66cd92f4e19c460cace200e213de3845.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/72c2cee1f9d744ca87e0c9a9121ce979.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/c6c30ad149ef4fcb85bdb668b918ac8a.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/0630c60c08314b1cb357935a91bdffb7.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/54ecbcefddda4198859643d1bc0d4874.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/8d5699061ff548e280141b131f8c8dfd.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/cdcba05f7bf74ea6998cc00e60046bbc.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/705bb4f394144d059e5d302a2446e1c3.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/1224f6b8ed9543b2a994a5ba77777137.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2bdf466d08f44388a43c39b6e8496761.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/3006ef54e71f46c695e7c14592957d94.png)

## 2.Hello,World!
### Visual Studio Code，我的编辑器
[Visual Studio Code 官网下载](https://code.visualstudio.com/Download)
![在这里插入图片描述](https://img-blog.csdnimg.cn/81c796901c894343a3f352aca6eab7ed.png)

![在这里插入图片描述](https://img-blog.csdnimg.cn/67d9c04d795140dfa111cc7b26aed71a.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/7ababebd9d6443cb8e398372dc285ac3.png)

![在这里插入图片描述](https://img-blog.csdnimg.cn/6f9b719fe4e34e5d909a110aca3b7b1d.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/6cecc6c76ce544579004f7e574f71520.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/eda9557d80674c62831ff257ad5c2eb7.png)
### 打印 Hello, world!
#### 创建项目目录

```bash
ultralinux@ultralinux-PC:~/Desktop$ mkdir ~/projects
ultralinux@ultralinux-PC:~/Desktop$ cd ~/projects
ultralinux@ultralinux-PC:~/projects$ mkdir hello_world
ultralinux@ultralinux-PC:~/projects$ cd hello_world
```
#### 编写并运行Rust程序

```bash
ultralinux@ultralinux-PC:~/projects/hello_world$ code .
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/c0f035dc764a498597f4b92b95ae7209.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/90784aee76ce40d898c1dbca3cf8fbab.png)

```rust
fn main() {
    println!("Hello, world!");
}
\\CTRL + S 保存
```

```bash
ultralinux@ultralinux-PC:~/projects/hello_world$ rustc main.rs 	//编译，Rust会输出一二进制可执行文件。
ultralinux@ultralinux-PC:~/projects/hello_world$ ls
```
|linux	|win  |
|--|--|
|  main  main.rs| main.exe  main.pdb  main.rs |

```bash
ultralinux@ultralinux-PC:~/projects/hello_world$ ./main //
Hello, world!
//在 Windows 上，输入命令 .\main.exe，而不是 ./main
```
Rust 是一种 预编译静态类型（ahead-of-time compiled）语言，这意味着你可以编译程序，并将可执行文件送给其他人，他们甚至**不需要安装 Rust** 就可以运行。
### 分析

```rust
fn main(参数或返回值) {
    函数体，函数体，我前面有四个空格哟，你看不到吧！ ;
    Println!("字符串（参数）， 字符串（参数）");
    println!("Hello, world!");
    
}
```

```rust
fn //声明
main //特殊函数——最先运行的代码
左花括号与函数声明置于同一行并以空格分隔，是良好的代码风格。
println! //打印（输出）
分号结尾（;） //代表一个表达式的结束和下一个表达式的开始
```
| 函数 |Rust宏（macro）  |
|--|--|
|println  | println! |

#### 保持良好的风格
```rust
ultralinux@ultralinux-PC:~/projects/hello_world$ rustfmt --version
rustfmt 1.5.1-stable (4b91a6e 2022-08-08)
ultralinux@ultralinux-PC:~/projects/hello_world$ rustfmt main.rs 
```

## 3.Hello,Cargo!

 - 我们把代码所需要的库叫做 依赖（dependencies）
 - 使用 Cargo 启动项目，则添加依赖项将更容易。

```rust
ultralinux@ultralinux-PC:~/Desktop$ cargo --version
cargo 1.63.0 (fd9c4297c 2022-07-01)
```
### 使用Cargo创建项目
```rust
ultralinux@ultralinux-PC:~$ cargo new hello_cargo //使用cargo创建项目
     Created binary (application) `hello_cargo` package
ultralinux@ultralinux-PC:~$ cd hello_cargo/
```
![在这里插入图片描述](https://img-blog.csdnimg.cn/ca9e7702efb74b15b56ac6e98d030ae4.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/25d20b03dbe54b5ab9c943d1d6571af7.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/70041b88511f42fa90c57e854a80c1cd.png)

![在这里插入图片描述](https://img-blog.csdnimg.cn/0f53902ee00c4089916ebb080a572510.png)
？？？？？？？？？？？？

```rust
ultralinux@ultralinux-PC:~/hello_cargo$ code .
```
### cargo.toml
![在这里插入图片描述](https://img-blog.csdnimg.cn/133f117118b6403ca3737de45eb46ed8.png)
- Cargo 配置文件的格式—— TOML (Tom's Obvious, Minimal Language)
- [package]，是一个 区域（section）标题，表明下面的语句用来配置一个包 （package） 。随着文件增加更多的信息，还将增加其他片段（section）。
	- name，项目名称
	- version，项目版本
	- edition，所须rust版本    [附录E](https://kaisery.github.io/trpl-zh-cn/appendix-05-editions.html)
	- authors，项目作者
-	[dependencies]，是罗列项目依赖的片段的开始。在 Rust 中，代码包被称为 crates。
### src/main.rs
![在这里插入图片描述](https://img-blog.csdnimg.cn/0926abd1e32f434381d231a756364b92.png)
- Cargo 将代码放在 src 目录，同时项目根目录包含一个 Cargo.toml 配置文件。
- Cargo 期望源文件存放在 src 目录中。项目根目录只存放 README、license 信息、配置文件和其他跟代码无关的文件。
- 若没有使用cargo创建项目，可以将其转化为一个 Cargo 项目。
	- 将代码放入 src 目录，并创建一个合适（相应的配置）的 Cargo.toml 文件。
### 构建cargo项目 cargo build
- 默认的构建方法是调试构建（debug build）
![在这里插入图片描述](https://img-blog.csdnimg.cn/f0d3140a6d184b57adf59292e8cf23de.png)
- Windows
![在这里插入图片描述](https://img-blog.csdnimg.cn/96a62b6ed2234c339c306e573e538ab3.png)
```rust
ultralinux@ultralinux-PC:~/projects/hello_cargo$ ./target/debug/hello_cargo		//运行可执行文件
Hello, world!
```

- Linux
![在这里插入图片描述](https://img-blog.csdnimg.cn/7ccb57dc1e5d4756adaee5fabb08b4a1.png)
```rust
PS C:\Users\ultra\projects\hello_cargo> .\target\debug\hello_cargo.exe		//运行可执行文件
Hello, world!
```
- 首次运行cargo build会在顶层目录创建一个新文件——cargo.look（记录项目依赖的实际版本）
	- 永远也不需要碰这个文件，让 Cargo 处理它就行了。

### 构建和运行cargo项目 cargo run
 1. cargo run——编译代码 + 执行结果
	- 若之前编译成功过，且源码未改变，那么就会直接运行二进制文件
![在这里插入图片描述](https://img-blog.csdnimg.cn/f58ab5eb063642caa850ea205bbd652c.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/b556103a61e44a8e90ad8f333a50d172.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/33472f527b7a44388f89ca19aac82dcd.png)


### cargo check
- 快速检查代码确保其可以编译但不产生可执行文件
- 编写代码时可以反复或定期运行 cargo check 确保它们可以编译。当准备好使用可执行文件时才运行 cargo build。
```rust
ltralinux@ultralinux-PC:~/projects/hello_cargo$ cargo check
    Finished dev [unoptimized + debuginfo] target(s) in 0.00s
```
### 为发布（release）构建
- cargo build --release
	- 编译时会进行优化
		- 代码会运行的更快，但编译时间更长
	- 会在target/release而不是.target/debug生成可执行文件
- 两种配置：
	- 一个开发，你需要经常快速重新构建；
	- 一个正式发布，不会经常重新构建，并且希望程序运行得越快越好。
	- 
测试代码的运行时间，请确保运行 cargo build --release 并使用 target/release 下的可执行文件进行测试。
### 尽量使用cargo，并把cargo当做习惯
？？？？？？
![在这里插入图片描述](https://img-blog.csdnimg.cn/4c42d5dc10574cbebf55e5573fceedf5.png)



