# 用闪光灯计时

> 原文：<https://hackaday.com/2019/11/24/keeping-time-with-blinkenlights/>

如果说这些年来我们学到了什么，那就是黑客喜欢怪异的时钟，他们喜欢在一个设备中装入尽可能多的彩色发光二极管。将这两个概念结合到一个项目中，你会得到一个完美的风暴。因此，就不必要的复杂时计而言，我们会说由[无畏之夜]打造的[“疯狂时钟 4”是有史以来最伟大的](http://www.fearlessnight.com/cc4/index.html)。

[![](img/35090207f5532e7f4874d556da2a8ace.png)](https://hackaday.com/wp-content/uploads/2019/11/crazyclock_anim.gif) 这款 Arduino Pro 迷你时钟通过 GPS 同步当前时间，带有温度补偿的 DS3231 RTC，使其在卫星下行链路之间保持平直。一旦时钟有了正确的时间，你怎么读它？嗯，在顶部你有一个正常人的基本数字读数，旁边有一个圆形的 LED 显示屏，看起来像是科幻电影道具。在较低的层次上，有一个用于真正展示的二进制时钟，如果这还不够，甚至还有双颜色编码的模拟仪表来显示小时和分钟。

从 Arduino 源代码到外壳的 3D 模型和定制 PCB 的 Gerber 文件,[Fearless Night]为您提供了在家学习所需的一切。就个人而言，我们认为时钟的上半部分对于我们的计时需求来说已经足够了。如果没有其他事情，它应该有助于节省一些能源，因为时钟目前在所有发光二极管关闭的情况下消耗了令人难以置信的 20 瓦。

如果你决定[沿着记忆之路](https://hackaday.com/2014/05/16/led-clock-looks-cool-and-tells-time/)走一走，看看我们过去介绍过的[其他有趣的 LED 钟](https://hackaday.com/2014/06/16/attiny84-powered-minimalist-led-clock/)，[你会忙上一阵子](https://hackaday.com/2014/10/26/star-gate-led-clock-has-plenty-of-pizazz/)。但是对于我们的钱来说，它仍然很难击败不可能迟钝的单 LED 时钟。