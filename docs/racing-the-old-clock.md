# 与旧时钟赛跑

> 原文：<https://hackaday.com/2020/12/23/racing-the-old-clock/>

[Keenan Rebera]最近发现自己有一个室友留下的旧赛车钟(chronoix cc3000)。这位室友是如何得到这样一个时钟的，这一点看起来很模糊，但 Keenan 毫不畏惧地开始工作，用蓝牙功能将时钟变得栩栩如生。数字的机械性质提供了令人满意的听觉点击，使其成为一些升级的良好候选。新的大脑移植是古老的 ESP32，带有 RTC。他创建了一个带有 QWIC 连接器的定制 PCB，将驱动板以菊花链形式连接在一起。每个 PCB 有四个 TBD62083 用于驱动数字，两个 MCP 扩展器用于增加地址空间。这使得 ESP32 能够处理 I2C 的所有不同网段。通过将不同的焊盘焊接在一起，他可以改变每个 MCP 的地址，最多给出 16 个数字(9 个可能的 MCP 每个驱动 2 个数字)。

一个设计精美的应用程序伴随着时钟，使更新 RTC 和设置时区变得轻而易举。目前，它正在显示 2020 年正式结束的倒计时。虽然 2020 年肯定会作为动荡的一年载入史册，但对于 Hackaday 的 DIY 时钟来说，这是伟大的一年。就在过去几周，我们已经看到了[大型 LED 车间时钟](https://hackaday.com/2020/11/01/big-workshop-clock-is-3d-printing-done-right/)、[深奥的多米诺骨牌时钟](https://hackaday.com/2020/11/12/domino-clock-tells-the-time-in-style/)和[兼作艺术品的漂亮时钟](https://hackaday.com/2020/11/01/brassy-classy-wifi-clock-shows-weather-too/)。到 2021 年，我们很有信心[Keenan]将仍然有一个华丽的时钟在他的墙上滴答滴答地走着。

 [https://www.youtube.com/embed/U6XVd7QMqqU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/U6XVd7QMqqU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Keenan]发送此邮件！