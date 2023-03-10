# 让幽灵般的猫头鹰告诉你天气

> 原文：<https://hackaday.com/2019/06/18/let-a-spooky-owl-tell-you-the-weather/>

很少有 20 世纪 70 年代的年轻读者不想分享《史酷比-杜》中无畏的动画《捉鬼少年》的冒险经历。你还记得这个系列中的什么？那辆*谜* *机*面包车？史酷比零食？或者是那些不太可能闹鬼的主题公园，如果不是因为那些讨厌的孩子，它们的主人可能已经逃脱了？对于[亚历克斯·莎士比亚]来说，这似乎是闹鬼图片的比喻，主题的眼睛会跟随房间里的主角，因为当他制作一个壁挂式天气指示器时，他给了它一只眼睛做同样事情的猫头鹰。

该设备的天气部分非常简单，一个 ESP8266 板驱动一组伺服系统，根据来自[黑暗天空 API](https://darksky.net/dev) 的数据移动刻度盘指示器。猫头鹰移动的眼睛是聚会的一部分，对它们来说，ESP 从 Adafruit AMG8833 热传感器阵列获得输入，并驱动伺服和杠杆装置来移动。最后，热感摄像机的输出可以在 ESP 的网络服务器上看到。项目的所有细节都可以通过[GitHub 库](https://github.com/shakso/owlweather)找到。

结果显示在休息时间下面的视频中，正如你可能期望的那样，它的灵感更多的是喜剧而不是困扰。但也许这是跟随观众的艺术品受欢迎的根源，其中[这仅仅是一长串](https://hackaday.com/2019/06/04/motion-tracking-face-really-does-follow-you-around-the-room/)中的最新一个。

 [https://www.youtube.com/embed/EZxBqRomFxc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EZxBqRomFxc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

