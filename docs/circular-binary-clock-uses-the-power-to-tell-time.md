# 圆形二进制时钟使用电源来显示时间

> 原文：<https://hackaday.com/2022/11/25/circular-binary-clock-uses-the-power-to-tell-time/>

时钟应该是圆的吗？我们认为这取决于时钟的样式。毕竟，我们不会期望看到一个带圆形读数的数字钟只是为了好玩。但是二进制时钟——那完全是另一种动物。虽然[JohnThinger]几周前用 RGB LED 条和 ATtiny 制作了一个线性二进制时钟，[他决定在第一轮](https://www.instructables.com/A-Circular-Binary-Clock/)中它会看起来更好。

在你谴责这个东西上有除了 1 和 0 以外的数字之前，这些数字只是 2 的幂，你必须乘以它才能得到时间。自然地，它分三个阶段完成，黄绿色数字代表秒，粉红色代表分钟，蓝色代表当前小时。不，重点不是让生活变得更容易。但它是一个好看的钟，不是吗？

就像以前一样，ATtiny85 是大脑，有一个 RTC 芯片和一个振荡器来保持时间。但是现在，显示器包括负空间 3D 打印的数字和 RGB LED 环。休息之后一定要去看看。

 [https://www.youtube.com/embed/OytrEbsJomI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OytrEbsJomI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

