# 从 USB Type C 获取电源

> 原文：<https://hackaday.com/2019/06/30/extracting-power-from-usb-type-c/>

在过去十年左右的时间里，我们一直在用 USB 为我们的便携式设备供电和充电。这是一个有效的系统。你用 DC 给电池充电，你不想每个设备都有一个壁式电源插座，所以只需抓住一个 USB 集线器，给你的手机和耳机或其他东西充电。现在，虽然，我们有 USB 类型 C，与电力输送。理论上，我们可以通过 USB 电缆获得 100 W 的功率。如果我们可以用螺丝终端接入呢？

这就是[Jakob]获得黑客日奖背后的想法。这是一个 USB 3.1 Type C to Type A 适配器，但它也有添加螺丝端子的整洁的小奖励。你可以把它想象成笔记本电脑或电话的跳线，但实际上*不会这么做*。

[Jakob]的板由一端的 USB 型插座和另一端的 A 型插头组成，而在这两个插座之间是一个 STM32G0 微控制器，用于处理电源协商和 PD 协议。这赋予了 USB Type C 端口双重角色端口(DRP)功能，因此电源连接可以双向进行。加上一个螺丝端子，理论上你可以通过一对电线得到 20 V 的 5 A 电压。玩得开心点。

现在，[Jakob]在 Gitlab 中有所有的文件[，这里有原理图和布局图](https://gitlab.com/jakob.faltisek/usb-type-c-with-pd-upgrade)。这是一个有趣的项目，有大量的 USB hackery 应用程序，有足够的能力做一些真正有趣的事情。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)