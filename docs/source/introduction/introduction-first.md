# 什么是Shell

Shell 是一个用 C 语言编写的程序，它是用户使用 Linux 的桥梁。Shell 既是一种命令语言，又是一种程序设计语言。
* 说到底要和Linux平台交互就要使用Linux命令，Shell就是使用linux命令编程，增加了很多语法比如条件语句和循环语句等，来实现一些较为复杂的功能。
* Shell就是一门编程语言。
* Shell 脚本（shell script），是一种为 shell 编写的脚本程序。
* 业界所说的 shell 通常都是指 shell 脚本，shell 和 shell script 是两个不同的概念。我们说的 Shell 编程，实际上写Shell脚本，而不是说修改Shell的源码。

## Shell的分类

Linux 的 Shell 种类有很多种，常见的有：

* Bourne Shell（/usr/bin/sh或/bin/sh）
* Bourne Again Shell（/bin/bash）
* C Shell（/usr/bin/csh）
* K Shell（/usr/bin/ksh）
* Shell for Root（/sbin/sh）
……

我们通常都是使用 Bash，也就是 Bourne Again Shell，Bash 也是大多数Linux 系统默认的 Shell。

有时候会看到一些脚本的头部标记了 `#!/bin/sh`，它同样也可以改为 `#!/bin/bash`，我们不区分 Bourne Shell 和 Bourne Again Shell。

## 格式

在编程的时候，当写成文件，要以`.sh`结尾，文件的开始要告诉系统用什么来解释这个脚本，比如`hello.sh`如下：

```bash
#!/bin/bash

echo hello world

```

`#!/bin/bash` 告诉系统，用`/bin/bash`来解释这个脚本文件。

## 文件在哪运行?

在任意Linux系统上运行，也可以随便在网上搜索 **在线Shell** 会出来一大把可以直接在线运行的网页。

## 应用场景

* 应用安装：我们都知道在 Linux 服务器经常需要我们安装配置一些软件或配置环境，人手工的一条命令一条命令执行，很容易出现错误，而且如果成百上千台服务器，那么此场景下 Shell 脚本就非常适合，编写一个应用安装配置脚本，后期可以重复使用，且不容易出错，Shell 脚本适用于重复性的工作；
* 定时任务：例如我们需要每分钟上报服务器的各项性能指标到监控服务端，此时可以写一个采集系统各项指标的脚本，然后配合定时任务来每分钟执行指标数据上报，Shell 脚本非常适用于周期性的工作；
* 应用操作：例如我们自己写的应用，可以为其编写启动 / 停止 / 重启等操作的脚本，将脚本添加进系统环境中，后期很方便进行服务管理；
* 备份恢复：可以利用脚本来进行网站文件或数据库的异地备份，以及恢复到测试环境进行验证等；
* CI/CD: Shell 脚本适用于 DevOPS 中的在服务器中持续集成持续部署的 pipeline 流程中，适用于应用发布最后一公里配置；
* 其他：当然 Shell 还可以做一些其他工作，比如运算 / 生成报表，甚至有大佬用 Shell 编写游戏等，可以根据自己的需求来利用好 Shell 脚本来为自己服务。
