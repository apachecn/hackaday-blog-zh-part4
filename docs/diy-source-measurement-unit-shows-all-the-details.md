# DIY 源测量单位显示所有细节

> 原文：<https://hackaday.com/2021/08/18/diy-source-measurement-unit-shows-all-the-details/>

SMU 或源测量单元的工作原理有点像电源，因为它可以将电流引入负载；有点像电子负载，因为它可以从电源吸收电流。它包括一个分频电路，因此它可以干净地、可预测地自动在宿和源模式之间切换。这使得它非常适用于测试各种电源电路、电池充电和特性化，或者通过替换两个独立的盒子来节省工作台空间。

[这款来自模拟电子大师[Dave Erikson]](http://www.djerickson.com/diy_smu/) 的 DIY SMU 是一款完整的四象限设计，这意味着它可以在正负电压下工作。该设计表现出优异的性能，可与昂贵的商业仪器相媲美，这证明了[Dave]的技能和经验。

![](img/9231b3194e87357240c09fa91ed87d89.png)

Source: Wikipedia

如果你想象一个横轴为电压，纵轴为电流的图表，象限就可以理解了。两个轴可以摆动到两个极性，象限 I 和 III 表示输送到负载的功率，象限 II 和 IV 表示从电源吸收的功率。

非常详细的项目日志显示每一个血淋淋的细节，发现的每一个问题和解决它的工作。这是一个很长的阅读，对于那些对此类设备感兴趣的人来说，这将是这个抄写员的愚见所花费的时间。

DIY-SMU 本质上主要是模拟的，控制部分由 Teensy 3.2 提供，用户界面是带触摸的 [Nextion](https://nextion.tech/) TFT 显示屏。固件甚至通过 USB 支持 [SCPI](https://en.wikipedia.org/wiki/Standard_Commands_for_Programmable_Instruments) ，以允许远程控制和数据收集，因此它可以直接放入您的测试和测量堆栈中。想了解更多的阅读益处，请查看 JSMU，一个相关的项目，从 DIY-SMU 中获得灵感。详情[可以在这个项目上找到 GitHub repo](https://github.com/jaromir-sukuba/J-SMU) 。

多年来，许多电源项目为这些页面增光添彩，比如这张 [2015 年 Hackaday 奖参赛作品](https://hackaday.com/2015/07/15/hackaday-prize-entry-a-better-bench-power-supply/)，但这是为数不多的四象限设计之一，所以请脱帽致敬！

 [https://www.youtube.com/embed/B26SW3N2zoA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/B26SW3N2zoA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[David Gustafik]的提示！