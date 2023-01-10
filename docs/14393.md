# 结合电子纸价格标签，创建一个大型无线显示

> 原文：<https://hackaday.com/2022/08/05/e-paper-price-tags-combined-to-create-a-large-wireless-display/>

在过去的几年里，电子纸价格标签在零售商店中变得流行起来，这对黑客来说是很好的，因为我们现在有一些更便宜的商品硬件可以玩。[Aaron Christophel]一直在创造带有电子纸价格标签的网格显示，直到 20×15 的网格。

电子纸价格标签非常适合这类项目，因为它们是无线的，重量轻，并且可以用板载电池持续很长时间。为了在胶合板背板上安装单独的标签，[亚伦]只需将 Velcro 粘到标签的背板上。显示器的固件基于【Dmitry grin Berg】的[逆向工程工作，使用方便的](https://hackaday.com/2021/03/28/a-deep-dive-into-e-ink-tag-hacking/) [3D 打印弹簧针编程夹具](https://www.youtube.com/watch?v=S44NSr37eoo&t=3s)闪存到几百个标签。所有的显示器都通过一个 Zigbee USB 加密狗控制，该加密狗插入运行工作站软件的 PC。

[Aaron]还在试验将显示器从外壳中取出，放入 3D 打印的网格框架中。缺点是丢失了电池座和天线，它们都集成在外壳中。他计划通过一个大电池为显示器供电，并通过 ISP 或 UART 将 ESP32 连接到显示器来解决这个问题。

这个项目紧随另一个使用蓝牙和一个相当聪明的更新方案的电子墨水网格显示项目而来。

 [https://www.youtube.com/embed/CLmotCeMlq0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CLmotCeMlq0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

