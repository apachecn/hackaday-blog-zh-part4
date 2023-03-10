# 修复夜灯的闪烁问题

> 原文：<https://hackaday.com/2020/01/31/fixing-the-flicker-afflicting-a-night-light/>

有些东西是很难舍弃的，即使它们已经坏掉了，本来就一文不值。但有些事情就是很特别，你知道吗？我们会说，在这种情况下，这东西绝对值得保存。

[【尝码】女儿心爱的小夜灯出现了可怕的闪烁问题](https://www.instructables.com/id/Fixing-and-Improving-a-Night-Light/)，然后彻底不工作了。为了让她开心，他打开盒子，发现其中一根电线从焊接的插座上断开了。这是一个足够简单的解决办法，但试图在墙壁是软塑料的狭小空间内焊接可能相当具有挑战性。

一旦这个问题得到解决，[品尝代码]将其插入一个测试插座。它恢复了工作，但也恢复了闪烁，因为没有电容器来平滑进入 led 的信号。[Taste the Code]测量桥式整流器输出端的电压降，并焊接在一个电解电容中，该电容的额定电压超过所需电压的两倍，以确保安全。休息之后你可以看看视频。

这说明了几件事:第一，你可以从当地的一元店学习修理和改进便宜的电子产品。第二，你还可以在那里以相当低廉的价格买到一些组件，比如基于磁性传感器的窗户报警器和非常便宜的太阳能庭院灯。

你还可以用那些为儿童设计的廉价宜家灯具做一些有趣的事情。[这是一个可爱的云灯，升级了 RGB LED，使用 ESP8266](https://hackaday.com/2019/06/12/ikea-cloud-lamp-displays-the-weather-with-esp8266/) 显示天气情绪。

 [https://www.youtube.com/embed/r1vrp6O3Sdo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/r1vrp6O3Sdo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

