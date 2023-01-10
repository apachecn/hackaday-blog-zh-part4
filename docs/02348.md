# 用简陋的 Arduino Uno 驱动无控制器 LCD

> 原文：<https://hackaday.com/2019/03/10/driving-a-controllerless-lcd-with-the-humble-arduino-uno/>

如今，你可能会认为用微控制器驱动液晶显示器很简单。廉价显示器大量涌现，准备在已经嵌入控制器的分线板上销售。加载正确的库，您可以在几分钟内启动并运行。然而，把你的注意力转到试图驱动你从一台旧设备中拉出的随机 LCD 上，事情突然变得更难了。伊凡·科斯托斯基正处于这样的境地，他决定开始工作。

[Ivan]的 LCD 是从旧磁带库中回收的 320×240 STN 设备。该显示器没有板载控制器，原始驱动程序也不容易重新利用。相反，[Ivan]决定直接从 Arduino Uno 上驾驶它。

这说起来容易做起来难。严格的时序要求推动了 8 位平台的极限，更不用说需要负电压来驱动屏幕和进一步的硬件来驱动背光了。这些都是依次解决的，[Ivan]分享了他的技巧，以获得最大的展示灵活性。讨论了图形和文本模式，以及通过对可用 RAM 和 flash 的各种使用可能实现的优化。

代码[可在 Github](https://github.com/ikostoski/arduino-clglcd) 上获得。如果你需要灵感来开发你自己的无控制器 LCD 驱动程序。[Ben Heck]也做过类似的工作，[使用 FPGA grunt 来完成这项工作。](https://hackaday.com/2015/01/29/reverse-engineer-then-drive-lcd-with-fpga/)