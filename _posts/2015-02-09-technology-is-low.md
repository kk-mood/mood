---
layout: post
title: 技术水平还是差的很远
categories: [砸碎]
---

今天在内网上看了一个技术分享，是讲的朋友圈的后台架构，还有一篇是讲朋友圈的数据存储架构。看之前以为马上就能学会屠龙之术了，相当高兴呐，结果看了才发现，卧槽，很多很多的东西都看不懂，实际工作经验不够，又没人来讲解，一个人看，很多东西理解不了。凭着聪明最多可以死记硬背的强记而已。看来还是得踏踏实实一步一步来提高。

今天听到一个小道消息，说我们现在的产品年后要加上 *LBS* 功能，这样可以查看附近的商店，现在还在讨论具体应该是怎么样的。我听到觉得这个不错，反正我是挺有兴趣的，多做、多接触东西总是好的。

今天还发现腾讯内网的一个权限漏洞，其实不应该说是漏洞，只是对内部员工的权限管理不是很严格而已。情况是这样的：我本来是没有内网的bbs权限的，也就是不能发帖、回帖、看帖，比如一些跳蚤市场、聚会交友(上面好多征男友的帖子)、租房信息等这些都属于bbs的范畴，我是没有权限，我的权限只是可以看看内网的其他模块，比如各种技术文章、技术月刊、讲座之类的。但是今天我装了一个手机版的 *km吧* ，发现在手机上就可以看到上面那些在pc上通过浏览器访问受限的模块了，看来移动端没有校验用户权限。移动端的权限阻碍只是在阻止你的下载和登录两部，因为下载和登录都需要token验证，因为我是做开发的缘故，正好有token，登录之后就校验权限了。而pc上的浏览器虽然也是可以通过token登录，但是在浏览器无论哪种登录方式都会有权限校验。相当于又让我钻了一空子，虽然意义可能并不是很大，但是钻空子这种事还是挺有意思的。


2015.02.09   22：20 
