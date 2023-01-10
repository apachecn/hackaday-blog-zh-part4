# 它是割草机吗？是 RPi IRC 服务器吗？都是！

> 原文：<https://hackaday.com/2021/04/09/is-it-a-lawnmower-is-it-an-rpi-irc-server-its-both/>

尽管最初是作为 4 月 1 日的一个笑话呈现在世人面前的，但[Jotun]的 [IRC 功能割草机](https://jotunheimr.idlerpg.net/users/jotun/lawnmower/)的诞生源于网下 IRC 网络上人们之间的随意玩笑。当这个项目比任何人预期的都要好时，它在 4 月 1 日被称为“T2 地下网络的绿色未来”。玩笑归玩笑，这个项目实际上非常有趣并且执行得很好。

核心是一个雷明顿 RM110，一个相当基本的气动推剪草机。在使用了几年后，它的运行不再那么好了，所以[Jotun]把它拆开并清洗了发动机，尽管以前从未这样做过。随着那项肮脏的任务完成，随后在 Undernet 频道上关于将割草机连接到 Undernet 的评论导致了 Raspberry Pi 4 和各种其他组件的订购。

[![](img/1504fc304a7f1d5f45c05966a4cdf5a5.png)](https://hackaday.com/wp-content/uploads/2021/04/lawnmower_irc_undernet_jotun_lawnmower.jpg)

The view from the driver’s seat with the server box installed.

[Jotun]的文章很好地概述了该项目的历史:从让树莓 Pi 4 与 UPS 插件一起工作，到让 IRC 服务器软件工作并为客户服务，以及将一个防风雨和防尘的盒子与足够的过滤通风放在一起，以确保新割的草不会阻塞树莓 Pi，同时保持一切凉爽。

作为奖励，该系统跟踪轮子的旋转，以便[Jotun]可以跟踪他修剪的平方公里的草，并通过 IRC 机器人向任何对 Undernet 感兴趣的人报告，在#lawnmower 频道。到目前为止，由于明显的振动问题，唯一不太好的是剪草机的实时摄像头，但[Jotun]认为这可以及时解决。