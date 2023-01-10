# 给木工车床增加数字读数

> 原文：<https://hackaday.com/2020/02/18/adding-a-digital-readout-to-a-wood-lathe/>

生活在现代的好处是，市场上有大量价格合理的机床供初露头角的制造商使用。然而，为了满足较低的价格点，产品往往放弃一些使工作更容易的功能。当然，如果你有自己做这件事的技能，这就不是问题了。

[扎克]喜欢使用他的木材车床，但它没有数字读数。谢天谢地，改造一个是一个简单直接的项目。经过一番研究，选择了霍尔效应传感器来检测车床的转速。因此，心轴安装了几个磁铁来触发传感器，从而比仅使用单个设备获得更高的分辨率。然后使用 Arduino Nano 监控霍尔效应传感器的输出，在一组 7 段显示器上显示转速。该项目然后得到了自己的定制 PCB，以及一个漂亮的 3D 打印外壳，以适应车床的身体。

这个项目展示了使用 maker 组件向基本机床添加功能是多么容易。这也证明了给项目一个合适的外壳的价值，使其能够在车间环境中生存。我们以前也见过其他的黑客 DRO 模式。休息后的视频。

 [https://www.youtube.com/embed/7gDZs0bImr0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7gDZs0bImr0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

