# 管理时间的完美有序的方法

> 原文：<https://hackaday.com/2018/12/23/a-perfectly-orderly-way-to-manage-your-time/>

[保罗·加拉格尔]花了数年时间将他的任务分成仔细测量过的块，这是一种被称为番茄工作法的时间管理方法。如果这还不足以证明他比普通黑客更有组织性和结构性，你只需要看一看他参加了电路雕塑比赛的这个华丽的番茄计时器。如果你突然觉得自己的时间管理技能不够用，不要惊讶。

[![](img/fed1c3e5284d1286171eeb64f5395064.png)](https://hackaday.com/wp-content/uploads/2018/12/wiretimer_detail-1.jpg) 虽然【保罗】传统上只是在头脑中记下他将工作分成的一小时一段的时间，但他认为是时候自己组装一个专用计时器来确保自己按计划运行了。当然，他可以使用商用定时器或手机上的应用程序，但他想做一些简单且不会引起任何分心的东西。一个容易启动，可靠，不做任何无关紧要的事情的计时器。我们不确定看起来像一个更先进的文明的产物是否是他的*官方*目标清单的一部分，但无论如何他设法实现了。

定时器分为两个主要部分:下半部分有控制器、USB 端口、一些无源元件和 ATmega328 微控制器，上半部分由三位 LED 显示屏组成。这两个部分由后侧的一个顶盖连接，这使得[Paul]无论出于什么原因需要重新安装计时器时，都可以很容易地将计时器拆开。设计中明显缺少 RTC 定时器持续时间相对较短(最长可达 95 分钟),这意味着 ATmega328 可以在可接受的漂移量内跟踪经过的时间。

计时器的显示侧确实是一个值得一看的景象，每个 LED 的腿焊接到一对精心弯曲的铜线上，以便它们与前面板的角度相匹配。相关电阻经过巧妙剪裁，使其主体平放在 PCB 上，而其引线则达到完美长度。这看起来像是一场维护的噩梦，但我们还是喜欢它。

随着我们[接近电路雕塑大赛](https://hackaday.io/contest/162559-circuit-sculpture-contest)的半程，还有足够的时间来提交你自己的功能艺术作品。如果你有一个项目避开印刷电路板来展示它，请在 Hackaday.io 上写下来，并确保在 2019 年 1 月 8 日截止日期之前提交。

 [https://www.youtube.com/embed/ZsGqnc2DhiA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZsGqnc2DhiA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

