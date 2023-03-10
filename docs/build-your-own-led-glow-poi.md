# 建立自己的 LED 发光 Poi

> 原文：<https://hackaday.com/2019/07/27/build-your-own-led-glow-poi/>

旋转 poi 是一种有趣的消遣，led 可以为这种体验增添一份精彩。[MilanDer]使用一些 maker staples 建造了一些他们自己的 LED poi。

首先创建一个 3D 打印外壳，使用“透明”PLA，实际上产生半透明的白色部分。这对内部的 APA102 LEDs 起到了很好的扩散作用。led 由 Arduino Pro Mini 驱动，它与降压升压转换器、锂电池和充电板一起安装在外壳内。最后，添加了一个带子，以允许用户轻松旋转 poi。

视觉效果非常好，通过使用红外接收器，可以远程控制 poi，只需按一下按钮，即可提供不同的 RGB 动画。我们希望看到一组旋转器，由于主控制器，它们具有同步的彩色 poi，这种硬件将能够胜任这项任务。

[我们以前也见过一些先进的联网 Poi](https://hackaday.com/2008/08/14/poiplay-led-poi/)。如果你有一个很棒的 LED 建筑，[一定要让我们知道。](http://hackaday.com/submit-a-tip)