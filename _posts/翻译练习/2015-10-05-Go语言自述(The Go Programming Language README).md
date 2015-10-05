---
layout: post
title: "Go语言自述(The Go Programming Language README)"
description: "Go是一门开源的编程语言，用它可以轻松地开发出简单、可靠、高效的软件。"
category: 翻译练习
tags: [Go]
---

{% include JB/setup %}

*声明：本文为笔者为练习英语所做的翻译练习，原文所属者与笔者没有任何关系，翻译结果不代表原文所属者的观点。笔者不保证翻译的正确性，任何人以任何形式的对本文的引用，都是不负责任和荒谬的行为，造成的后果笔者不予负责。*


**[原文链接](https://github.com/golang/go/blob/27ee719fb32b47b9bc59921e457f4b1e7f767968/README.md)**  
**所属:[golang/go](https://github.com/golang/go)**  


> Go is an open source programming language that makes it easy to build simple,reliable, and efficient software.

Go是一门开源的编程语言，用它可以轻松地开发出简单、可靠、高效的软件。

![Gopher image]({{ site.url }}/images/2015-10-05/fiveyears.jpg)

Go语言吉祥物Gopher（囊地鼠，产自北美的一种地鼠）

> For documentation about how to install and use Go, visit https://golang.org/ or load doc/install-source.html in your web browser.

如果你想知道如何安装和使用Go语言，请访问 https://golang.org/ ，或者在浏览器中打开该项目下的 doc/install-source.html 文件。

> Our canonical Git repository is located at https://go.googlesource.com/go. There is a mirror of the repository at https://github.com/golang/go.

我们权威的Git仓库位于 https://go.googlesource.com/go 。在 https://github.com/golang/go 中也有一个仓库镜像。

> Go is the work of hundreds of contributors. We appreciate your help!

Go语言是成百上千名参与者无私奉献的结果，我们非常重视和感激你的帮助！

> To contribute, please read the contribution guidelines: https://golang.org/doc/contribute.html

如果你愿意贡献一份力量，请查看贡献指南： https://golang.org/doc/contribute.html

> Note that we do not accept pull requests and that we use the issue tracker for bug reports and proposals only. Please ask questions on https://forum.golangbridge.org or https://groups.google.com/forum/#!forum/golang-nuts.

注意，我们不接受合并请求，我们只使用议题追踪来处理Bug报告和建议。请在 https://forum.golangbridge.org 或 https://groups.google.com/forum/#!forum/golang-nuts 上提问。

> Unless otherwise noted, the Go source files are distributed under the BSD-style license found in the LICENSE file.

除非另有说明，Go语言软件开发工具包的源码文件遵守BSD许可证来分布，你可以在LICENSE文件中查阅BSD许可证的详细条款。

--

> ## Binary Distribution Notes

## 二进制文件分发版说明

> If you have just untarred a binary Go distribution, you need to set the environment variable $GOROOT to the full path of the go directory (the one containing this file).  You can omit the variable if you unpack it into /usr/local/go, or if you rebuild from sources by running all.bash (see doc/install-source.html). You should also add the Go binary directory $GOROOT/bin to your shell's path.

如果你刚解压一个Go语言软件开发工具包分发版文件，你需要设置环境变量$GOROOT为软件开发工具包所在目录的完整路径，如果把它解压到了/usr/local/go目录下，或者你通过运行all.bash文件（详见doc/install-source.html）重新编译了，你可以省略这一步。你同样需要添加工具包中的可执行文件所在目录 $GOROOT/bin 到你的终端路径中。

> For example, if you extracted the tar file into $HOME/go, you might put the following in your .profile:

举个例子，如果解压了压缩文件到 $HOME/go ，你应该把下列语句添加到你的.profile文件中：

	export GOROOT=$HOME/go
	export PATH=$PATH:$GOROOT/bin

> See https://golang.org/doc/install or doc/install.html for more details.

如果你想了解更多，请访问 https://golang.org/doc/install 或查看 doc/install.html 。