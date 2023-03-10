# OptoGlitch 是专为失真设计的光耦合器

> 原文：<https://hackaday.com/2019/02/20/optoglitch-is-an-optocoupler-built-for-distortion/>

当我们关注信号的精确再现时，失真和噪声是工程师花费大量时间尽可能消除的敌人。然而，人类是不完美的生物，我们有时希望我们的媒体有点波纹和纹理——通常是模拟的，因为数字失真的阶跃变化可能会非常痛苦。厌倦了 Instagram 滤镜，想要采取不同的方法，[Patrick Pedersen]创建了[opto glitch——一种模拟失真的硬件解决方案。](https://github.com/UniQHW/OptoGlitch)

![](img/407accde74282b464a950b189bab3a12.png)

Changing the number of samples per pixel varies the accuracy of reproduction of the original image, left.

操作的概念很简单——通过改变 LED 的强度来发送数字图像的像素值，然后由光敏电阻拾取并重新数字化。由于不完善的传输过程，重新数字化的图像会受到各种失真和噪声的影响。

在 OptoGlitch 硬件中，LED 和光敏电阻故意对环境光开放，以进一步允许传输过程中出现噪声和失真。使用各种校准方法来避免结果完全无法识别，并且有各种定时和采样参数可用于改变最终效果的强度。

也有可能更有意地引入失真—[比如这个项目，它将元数据隐藏在畸形的字形中。](https://hackaday.com/2018/05/31/distorted-text-says-a-lot/)