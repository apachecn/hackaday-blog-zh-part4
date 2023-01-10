# 像 HUD 一样的时钟是一个透明的时间显示

> 原文：<https://hackaday.com/2022/12/14/hud-like-clock-is-a-transparent-time-display/>

虽然现在我们有各种类型的显示器，但那些看起来漂浮在空中的显示器有一些特殊之处。这个来自[几维丛林步行者] 的 [HUD 时钟就是这样一个例子。](https://www.instructables.com/HUD-like-WiFi-Sync-Clock-Transparent-Dot-Matrix-Di/)

该构建依赖于四个 8×8 LED 矩阵来显示组成时间的四个数字，由 MAX7219 驱动芯片运行。然而，led 不能被直接看到——那就太简单了。相反，矩阵将光线以一定角度射向一块倾斜的透明丙烯酸树脂。这就产生了一种“抬头显示”的效果，数字看起来像是漂浮在空中。该时钟通过 WiFi 从 NTP 时间服务器获得准确的时间，这要感谢运行该节目的 ESP32 微控制器。

在许多方面，这是一个简单的时钟，但我们特别喜欢平视显示技术的使用。几乎令人惊讶的是，我们并没有更经常地看到这些项目，比如汽车仪表板显示器或 T-16 陆地飞车中的 womp 老鼠。如果你一直在做你自己的 HUD 项目，[不要犹豫，通知 tipsline！](http://hackaday.com/submit-a-tip)

 [https://www.youtube.com/embed/316dtHW_6RE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/316dtHW_6RE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

