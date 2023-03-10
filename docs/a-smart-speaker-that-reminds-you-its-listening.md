# 提醒你它在听的智能扬声器

> 原文：<https://hackaday.com/2020/10/15/a-smart-speaker-that-reminds-you-its-listening/>

[markw2k9]有一个 Alexa 设备，放在他的厨房里，他决定是时候用一些相当不可思议的眼睛来装饰它了。受展示类似动画眼睛的 [Adafruit 诡异眼睛项目](https://learn.adafruit.com/animated-electronic-eyes/overview)的启发，[markw2k9]设计了一个 3d 打印外壳，放在第二代亚马逊 Echo 的上面。一个 teensy 3.2 为两个有机发光二极管显示器供电，并监控光环，以知道何时开灯，并显示您的智能扬声器正在收听。眼睛以一种诡秘的方式四处张望。来自 echo 的 LED 环的光通过一块在外环上轻轻打磨的有机玻璃扩散，眼睛镜片是 30 毫米的凸圆形(通常用于珠宝的玻璃镜片)。

一个问题是，当有通知时，Echo 上的环会以稳定的模式发光。由于这将导致 OLED 几乎持续开启，并影响有机发光二极管面板的寿命，因此决定在状态机中检测这种情况，并进入超时状态。随着这个问题的解决，整个事情变得很好。这个项目真正出彩的地方是设计和执行。该案件是圆滑解放军和整个事情看起来专业。

我们已经看到了一些受动画眼睛项目启发的其他项目，例如这个万圣节主题机器人，老实说，它非常可怕。智能音箱眼睛[的软件和 STL 文件在 Github](https://learn.adafruit.com/animated-electronic-eyes/software) 和 Thingiverse 上。

 [https://www.youtube.com/embed/jPCRWrPq4II?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jPCRWrPq4II?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[markw2k9]发来这一篇！