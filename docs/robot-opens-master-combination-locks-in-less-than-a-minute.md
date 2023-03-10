# 机器人不到一分钟就打开了主密码锁

> 原文：<https://hackaday.com/2022/09/18/robot-opens-master-combination-locks-in-less-than-a-minute/>

银行抢劫 B 级电影中一个常见的比喻是有人毫不费力地绕过了保险箱的密码锁。通常，英雄或恶棍会在听内部机械装置时转动转盘，然后根据锁发出的声音推断出密码。在现实生活中，高质量的密码锁不容易受到这种简单的攻击，但廉价的密码锁往往可以不费吹灰之力就被绕过。有些非常简单，这一过程甚至可以自动化，正如[Mew463]通过建造一台可以在不到一分钟的时间内打开主密码锁的机器所展示的那样。

[![A machine that holds a combination padlock and turns its dial](img/a9045bd38bc5a1f418b800c7d451d55a.png)](https://hackaday.com/wp-content/uploads/2022/09/Master-Lock-Picker-working.gif) 工作原理基于几年前萨米·卡姆卡的[研究。对于某些类型的主锁，可以通过在钩环上施加少量压力并在表盘上搜索其移动变得更重的位置来找到密码。然后可以使用一个简单的算法来完全确定第一个和第三个数字，并为第二个数字找到一个只有八个候选数字的列表。](https://hackaday.com/2015/05/17/cracking-a-combo-lock-in-under-30-seconds/)

[Mew463]的机器通过步进电机转动转盘，并使用伺服系统和齿轮齿条系统拉动钩环，从而自动完成这一过程。磁性编码器安装在步进电机上，以确定电机何时停止，而伺服系统的内部位置编码器作为检测钩环移动距离的手段。所有这些都由安装在定制 PCB 上的 Arduino Nano 和 TMC2208 步进驱动器控制。

正如你在下面嵌入的(无声)视频中所看到的，这台机器平稳而快速地完成了它的工作。所有的设计文件都可以在该项目的 GitHub 页面上找到，所以如果你有一抽屉没有组合的锁，你有机会让它们变得有点用。毕竟，这些锁的漏洞已经有很长的历史了，我们甚至在 T3 之前见过 T2 的自动破解程序。

 [https://www.youtube.com/embed/nw5f3ZPQd-o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nw5f3ZPQd-o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

