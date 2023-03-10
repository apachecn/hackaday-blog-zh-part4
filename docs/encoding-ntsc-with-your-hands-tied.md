# 束缚手脚编码 NTSC

> 原文：<https://hackaday.com/2022/12/25/encoding-ntsc-with-your-hands-tied/>

一般来说，当试图实现某个协议时，会受到硬件和时间的限制。但对于像[EMMIR]这样的人来说，这还不够。例如， [NTSC-CRT 是一个视频信号编码/解码模拟器](https://github.com/LMP88959/NTSC-CRT)，没有硬件加速、浮点数学或第三方库。只是基础 c。

虽然 NTSC 已经正式在美国销声匿迹，但人们仍然在 T2 制造自己的电动发射机。NTSC 是一个有点奇怪的标准，有时被称为[永不两次相同的颜色](https://hackaday.com/2016/10/06/never-twice-the-same-color-why-ntsc-is-so-weird/)，但它确实产生了独特的外观。

那种表情正是[EMMIR]想要的。它将 ppm 格式的消息编码为 NTSC，然后再编码为 ppm 格式，并带有一些可配置的噪声。它可以在[EMMIR 的]引擎中或通过 CLI 在渲染图像上实时实现这一效果。看起来很不可思议，还有很满足的东西。休息后有一个视频展示效果。代码非常短，易于阅读。

 [https://www.youtube.com/embed/ucfPRtV6--c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ucfPRtV6--c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

