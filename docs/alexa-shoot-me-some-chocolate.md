# Alexa，给我一些巧克力

> 原文：<https://hackaday.com/2020/05/11/alexa-shoot-me-some-chocolate/>

[Harrison]一直在忙着寻找隔离更好的一面，建造了一个语音控制、面部跟踪的 M & M 发射器。这个精心设计的糖果发射器不仅可以控制弹药的角度、方向和速度，还可以自己定位和锁定目标。

科学来了:[Harrison]骗 Alexa 以为机器里面的树莓 Pi 是一台名为[Chocolate]的智能电视。他只是告诉一个回声增加音量，无论他想要多少糖果色的投射物射向他的脸。然而，仅仅知道秘密语言是不够的。多亏了一点基于面部的安全措施，你几乎必须是[哈里森]或者他的替身才能得到糖果。

Pi 拍摄照片，寻找人脸，并使用 Arduino Nanos 驱动的三个伺服系统在该方向旋转炮塔底座。然后 Pi 进行面部标志检测，在计算完美抛物线和开火之前找到目标的嘴部孔。正如[Harrison]在下面的优秀构建视频中指出的，这台机器使用由 DC 电机驱动的飞轮，而不是弹簧加载的。M & Ms 巧克力豆从斜道上移动一小段距离，碰到一个灵活的旋转圆盘，像投球机一样投掷出去。

如果你不想让你的脸出现在 Alexa 上，我们会理解的。没事— [你还能有个声控糖果炮](https://hackaday.com/2016/09/12/licorice-launcher-locks-on-to-your-voice/)。

 [https://www.youtube.com/embed/hsGhCl0y1FY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hsGhCl0y1FY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

