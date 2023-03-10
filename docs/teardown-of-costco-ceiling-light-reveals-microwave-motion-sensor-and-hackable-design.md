# Costco 吸顶灯的拆卸揭示了微波运动传感器和可拆卸设计

> 原文：<https://hackaday.com/2020/03/30/teardown-of-costco-ceiling-light-reveals-microwave-motion-sensor-and-hackable-design/>

[hclxing]急切地拿起一个 LED 吸顶灯，因为它能够远程打开和关闭，但事实证明，这种灯还有很多其他功能。其中包括可调亮度、色温、自动关闭、光线感应、运动感应等等。在安装之前，[hclxing]决定[把它拆下来，看看是什么让所有这些功能发挥作用](https://hclxing.wordpress.com/2019/11/26/tearing-down-a-costco-remote-ceiling-light/)，但是打开灯之后，没有什么可看的。令人惊讶的是，除了装满 led 的 PCB 之外，该装置内部只有两个组件:一个交流电源适配器和一个小型白色控制器单元。就是这样。

[![](img/00f9baad3e3e8a29a68e8cd421bd6bbe.png)](https://hackaday.com/wp-content/uploads/2020/03/Microwave-Motion-Sensor-Board-on-Controller.jpg)

Microwave-based motion sensor board on top, controller board for LED ceiling light underneath.

电源适配器很简单，它接受 100-240 伏交流电，并将其转换为 30-40 伏 DC 供 led 使用，它似乎也为控制器提供 5 伏电压。但是[hclxing]注意到这个白色的控制器单元——除了 led 之外唯一的其他组件——上面有一个 FCC ID。一个快速的网上调查显示，ID 是附在一个微波传感器模块上的。我们大多数人可能会期望看到一个 PIR 传感器，但这种光是微波运动感应。我们[在过去](https://hackaday.com/2019/06/11/reverse-engineering-wyzesense-hardware/)看到过这样的单元测试，链接到一个视频【hclxing】也参考。

这里显示的是微波运动传感器板，下面是一个控制所有其他功能的高密度 PCB。一旦[hclxing]确定了电线和它们的信号，好市多就可以购买更多，因为这种设备看起来非常容易被黑客攻击。鉴于他们过去对 WyzeSense 硬件进行逆向工程的历史，我们确信[hclxing]可以做到这一点。