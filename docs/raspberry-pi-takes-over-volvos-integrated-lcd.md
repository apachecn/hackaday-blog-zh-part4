# 树莓派接管沃尔沃的集成液晶显示器

> 原文：<https://hackaday.com/2021/02/05/raspberry-pi-takes-over-volvos-integrated-lcd/>

正如[Luuk Esselbrugge]在最近的一篇博客文章中解释的那样，他的 2002 年沃尔沃 S60 有一个可选的 GPS 导航系统和备用摄像头，它使用一个电动显示器，在需要时会从仪表板上升起。他的特殊汽车没有安装硬件，但在他拿到一个显示模块并做了一些研究后，[他想出了如何用 Raspberry Pi 和几个微控制器来驾驶它。](https://luuk.cc/p/vD2f/Android_Auto_on_Volvo_RTI)

鉴于显示器的年龄，你可能不会惊讶地听到它使用复合视频。不完全是高分辨率，但在休息后的演示中，我们不得不承认它看起来超过了任务。[Luuk]正在通过 openauto 项目在 Raspberry Pi 3 上运行 Android Auto，这给他提供了一个漂亮的大显示屏，并可以访问你所期望的所有导航和媒体应用程序。显示器不支持触摸，但多亏了插入 CAN 总线的 ESP32，他能够通过读取沃尔沃方向盘上的按钮来控制软件。

[![](img/1b94c057e5065a2fb27b032c243ffdee.png)](https://hackaday.com/wp-content/uploads/2021/02/volvopi_detail.jpg)

Composite video sources are switched with a simple relay.

为了真正提升和降低显示器，[Luuk]发现你只需要沿着显示器线束中内置的 1200 波特串行总线发送几个字节。ESP32 也处理这一任务，至少部分是因为它已经插入了 CAN 总线，可以判断车辆何时倒车。如果 Pi 没有要求提高显示，这就允许它调出屏幕来显示来自新安装的备用摄像机的视频。顺便说一下，插上电话通常会触发系统唤醒并升起屏幕，断开电话会命令屏幕降回收起位置。

细心的读者或沃尔沃爱好者可能想知道[Luuk]是如何让音频工作的。由于他的汽车音响系统没有辅助输入功能，他正在使用 Arduino 来欺骗 CD 换碟机的存在，这允许他将音频信号注入收音机背面的一个引脚。最终，他想将这项任务转移到 ESP32 上，但他说，像这样的大变化必须等到天气转暖。

这不是我们第一次看到树莓 Pi 被用来为一辆有点老的车增加增强功能。虽然有些人哀叹现代车辆越来越复杂，但似乎有些黑客无法满足。

 [https://www.youtube.com/embed/8EuZUeXEYJ4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8EuZUeXEYJ4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

