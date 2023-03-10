# LED 灯泡已经达到最终(也是最便宜的)形式了吗？

> 原文：<https://hackaday.com/2020/02/16/have-led-bulbs-reached-their-final-and-cheapest-form/>

[electronupdate]多年来做了许多 LED 灯泡拆卸工作，见证了越来越便宜和越来越简单的实现方式，并怀疑 LED 灯泡设计最终达到了它的最终目标。最近一家一元店的拆除例子表明，成本削减已经成功地削减了这个看起来已经充满低价设计的市场。

这个发光的成本削减模型中的电气组件包括一个 PCB ( [以前看到的一元店 LED 灯泡示例有两个](https://hackaday.com/2017/10/11/dollar-tree-led-bulb-tear-down/))、11 个 LED、一个桥式整流器、两个电阻器和一个控制器 IC。为以防万一，线绕电阻器显然也可用作保险丝。

[![](img/1c1717b70e33d3806ba1dff2cc8d5a3c.png)](https://hackaday.com/wp-content/uploads/2020/02/dollar_store_led-0001.jpg)

Inside the unmarked controller IC. The design is as cheap as it is clever in its cost-cutting.

这还不是全部。[electronupdate]不仅仅是简单的拆卸，还打开了控制器 IC 的盖子，看看里面藏着什么，结果如下所示。这个控制器负责从桥式整流器和大电解电容提供的约 100 伏 DC 驱动 led，它既便宜又聪明。

上半部分是一个用于斩波电压的大晶体管，下半部分是简单的控制逻辑；操作速度足够快，led 不会出现闪烁，也不需要输出平滑电容。当然，结果是更少的元件和更低的成本。

你们中的一些人可能记得，在 LED 照明的早期，可以持续 10 万小时的灯泡是一个热门的承诺。由于各种原因，这种情况并没有发生,向成本至上的日常消费品的进军仍在继续。[electronupdate]认为他们可能已经达到了最终目标，至少在其他事情发生变化之前是如此。它们很好用，很便宜，而且几乎所有其他东西都被成功地撬开并扔出了门外。