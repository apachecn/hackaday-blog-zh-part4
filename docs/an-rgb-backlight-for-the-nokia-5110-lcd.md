# 诺基亚 5110 液晶屏的 RGB 背光

> 原文：<https://hackaday.com/2020/07/04/an-rgb-backlight-for-the-nokia-5110-lcd/>

硬件黑客喜欢诺基亚 5110 液晶显示器。或者至少，他们喜欢它的复制品。你可以在任何出售电子零件的地方花几块钱就能买到这样的面板，由于到处都是代码和文档，将它集成到你的项目中是很容易的。虽然它可能便宜可靠，但它不是一个非常令人兴奋的组件。

这也许就是为什么[【米格尔·赖斯】认为他应该用 RGB 背光](https://docs.microinventions.net/designs/rgb-backlit-nokia-5110-lcd)来装饰一下。虽然我们承认这个技巧主要是为了看起来很酷，但它并不完全是没有实际应用的*。如果你的小玩意出现了某种故障，让它在 LCD 上闪着亮红色肯定会引起房间另一端的人的注意。*

[![](img/60435fa79233c16bd67afa72e7cf2ac8.png)](https://hackaday.com/wp-content/uploads/2020/06/rgbnokia_detail.png) 电路板本身非常简单，四个 MHPA1010RGBDT RGB LEDs 和几个无源器件让它们保持快乐。诺基亚 5110 LCD 模块就这样弹出来了，除了为三种 LED 颜色添加的额外引脚之外，还像以前一样接线。背光 led 只需要微控制器上的几个备用 GPIO 引脚来驱动它们，就可以了。

[【Miguel】目前正在 Tindie](https://www.tindie.com/products/microinventions/rgb-nokia-5110-lcd-board/) 上出售他的这款标志性 LCD 的 RGB 版本，价格仅比标准版本高几美元，所以这看起来是为你的下一个项目增加一点光彩的一种非常便宜的方式。(Tindie 归 Supplyframe 所有，后者还拥有 Hackaday。但是他们没有让我们添加这个链接。)