---
layout: post
title: 近期面试题目汇总
categories: [work]
---

最近我又出去面试，原因不是这里的重点，不多说，下面只罗列一下碰到的一些题目，所有的题目都是来自于一个公司—— *腾讯* ！

根据面试时间先后顺序，题目如下：

1. C/C++的关键字—— *volatile* .
2. HTTP是有状态的还是无状态的协议？
3. 进程间怎么传递描述符？
4. 字节长度的问题：32位机器，int，long, 指针等各占多少字节？
5. 编程：实现一个`strncpy(const char* src, char *dest);` 函数。
6. 编程：实现一个非递归的二叉树遍历。
7. 编程：一个数组 *n* 个元素，其中有一个重复，找出重复的那一个元素。
8. 互斥锁和读写锁的区别？
9. 当访问量从100w上升到1000w，1亿，10亿时会碰到什么问题，怎么解决？
10. `cat /etc/passwd | grep users >> tat.txt &` 这个过程执行了哪些系统调用？
11. mysql 中 100万条记录，怎么快速过滤出自己想要的数据？
12. HTTP连接过程中，哪一方先断开连接？
13. select 和 epoll 的最大区别？
14. redis的特性是什么，备份机制是什么？
15. memcached 的网络模型是什么？线程模型是什么？
16. 有64匹马，8个跑道，至少比赛多少次可以选出前四名。不能给每匹马计时。
17. 编程：实现冒泡排序。
18. 有20个球，两个人轮流拿，每次可以拿的数量为：1，2，4. 拿到最后一个球的人输。问：先拿必胜还是后拿必胜，有没有固定的策略可以赢。
19. 口袋里有黑球和白球各100个，每次从口袋中拿出两个球，如果颜色相同，放入一个黑球，如果颜色相异，放入一个白球，问：最后一个球是黑球的概率？
20. 有一个数组，每个数字都出现了两次，只有一个数字出现了一次，找出只出现了一次的数字。
21. 系统设计题：缴费系统和银行对接，满足以下条件：1.服务要可靠，不能提示成功，银行却没收到钱；2.服务宕机或者网络不可用，要保证用户正常使用；3.比如月末流量突增，也要有应对措施；4.银行接口经常不稳定，这种情况要保证好的用户体验。
22. C++，构造函数和析构函数是否都可以为虚函数？
23. class中， static成员占不占用class的内存空间？
24. fork函数的返回值在子进程和父进程各是多少？
25. 写一个shell脚本，查看某个进程是否存在，比如/usr/bin/ppp, 如果不存在，则输出警告信息并启动进程。
26. 编程题：写一个函数，找出字符串中是否有重复的字符，如果有返回1，没有返回0，`int fn(const char *inputstring);` .
27. 算法题：有1000个苹果，要装进10个箱子中，问是否有一种方法可以满足：无论想要多少个苹果，都可以整箱整箱的拿取。 如果是100万的苹果和20个箱子呢？
28. 编程题：实现系统函数`int atoi(const char *input);` 字符串转整数。
29. 系统设计题：设计一个feeds的存储系统，有10亿用户，要求：1.可以通过用户维度进行查看数据；2.可以根据时间点进行查看数据。
30. 有1000万手机号在文件中，有重复的，找出重复最多的前10个。
31. list和vector的区别，适用场景？
32. set和map的区别，适用场景？
33. 从源码层面上讲讲memcached 的流程和架构。
34. tcp的三次握手和四次握手。
35. 常上哪些网站？
36. 有两个桶，4L和 6L，现在要取 3L 的水，可能吗？ 怎么做？ 如果把 4 改成 5L， 可以吗，怎么做？
37. 编程题：实现一个二分查找函数？
38. 编程题：long long 类型的本机字节序转换为网络字节序。
39. 编程题：一个字符串函数，找出重复次数最多的字符和重复的数量。
40. coredump文件，怎么处理它？
41. 一个服务总是超时，怎么去排查原因？
42. 工作里面都有什么有意思的项目？


上面基本就是这一个月碰到的面试题。

2015.09.23
