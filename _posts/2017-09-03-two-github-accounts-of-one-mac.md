---
layout: post
title: 一台Mac上使用两个Github账户的ssh-key
categories: [折腾]
---

### 背景 & 问题

昨天突然想到一个tricks，需要有两个Github账户，所以我又去开了一个小号，在我把ssh-key添加进github-02账户的时候提示我这个ssh-key已经被使用了，不能再使用。后面搜索了一下发现，同一个ssh-key只能添加到一个Github账户中，所以需要找到一个解决方法来解决：一个电脑使用两个Github账户（或者说类似的Git账户）。

### 方法

#### 0x01

生成新的ssh-key：

```shell
$ ssh-keygen -t rsa -C "your-email-address”
```

当提示输入名字的时候，输入新的文件名：<font color="red">id_rsa_2</font>。这时  `~/.ssh/`  目录中应该有两个这几个文件：`id_rsa, id_rsa.pub, id_rsa_2, id_rsa_2.pub` 。

#### 0x02

添加新的ssh-key到新的Github账户。

#### 0x03

在本地添加ssh-key的配置文件，在 `~/.ssh/` 中的新建config文件，添加如下代码：

```
# 这个是为了已有的Github账户使用
Host github.com
HostName github.com
IdentityFile ~/.ssh/id_rsa
# 这个是为了新的Github账户使用
Host <font color="red">alias_name</font>
HostName github.com
IdentityFile ~/.ssh/id_rsa_2
```

其中标红的部分是一个别名，可以随便起一个名字，在后面还会多次用到，所以用了红色标记。

#### 0x04

测试是否能连通：

$ ssh -T git@github.com
Hi your_name! You've successfully authenticated, but GitHub does not provide shell access.
$ ssh -T git@<font color="red">alias_name</font>
Hi your_second_name! You've successfully authenticated, but GitHub does not provide shell access.

有这样的输出表示和两个账户连接正常。

#### 0x05

clone项目改动点，我们一般使用的以下命令来clone一个远程仓库：

$ git clone git@<font color="red">github.com</font>:github_user_name/project_name.git 

这个时候，对于Github账户2的项目，需要把红色部分替换为上文中的 *alias_name*,即这clone命令为：

$ git clone git@<font color="red">alias_name</font>:github_user_name/project_name.git

对于已存在的git project，可能也需要通过下面的命令来从新设置远程的地址：

$ git remote set-url origin git@<font color="red">alias_name</font>:github_user_name/project_name.git

现在已经就可以无感知的使用ssh方式push代码了。

### 总结

网上有不少写这个方法的文章，但是感觉都长得一样，而且流程不连贯，实际操作起来可能会脱节，导致不知道问题出在哪里，所以自己写了这篇，算是一个备忘吧。

2017.09.03 11:42


