# 巧妙的机制很容易自动拉窗帘

> 原文：<https://hackaday.com/2021/08/29/clever-mechanism-easily-automates-pulling-the-blinds/>

我们都同意我们讨厌的事情很少，而闹钟的刺耳声音把你从美妙的睡眠中吵醒绝对是最讨厌的事情。为了更自然地醒来，【nutstobutts】创造了一个[自动窗帘开启器](https://github.com/Valar-Systems/model-s)。

![the automated curtain's driving motor](img/65032c26672b1f2419af93d64cc28fac.png)

开幕机很简单；控制箱中的步进电机拉动一根绳子，绳子穿过窗帘杆远端的惰轮，穿过两个夹子，连接到每个窗帘的背面。这种设计使得两个窗帘可以同时平稳地打开，并且总是在中间位置再次关闭。这种设计特别适合住在宿舍或公寓的学生，因为安装时不需要在墙上安装螺丝，也不需要对窗帘进行永久性修改。

窗帘可以通过按下控制箱上的按钮或向控制一切的 ESP32 发送 HTTP 请求来打开和关闭。这允许与许多不同的物联网系统集成，例如[nutstobutts]已经让 Home Assistant 在每天早上 6:30 打开窗帘，代替闹钟，然后在早上 9:00 自动关闭窗帘，以帮助节省冷却成本。

如果你只是想尝试一下，自动化窗帘是一个很好的物联网项目，[看看我们几个月前介绍过的不同风格](https://hackaday.com/2020/08/19/automating-mini-blinds-the-rental-friendly-way)以获得更多灵感！

[通过 [r/functionalprint](https://www.reddit.com/r/functionalprint/comments/pbdz9i/this_is_a_smart_curtain_opener_that_ive_created/)