# 使用这款开源 AVR 风扇控制器保持凉爽

> 原文：<https://hackaday.com/2021/03/12/keep-cool-with-this-open-source-avr-fan-controller/>

我们都有一些项目，我们没有时间为自己的目的记录下来，更不用说暴露在互联网的强光下了。一天只有那么几个小时，让我们面对现实吧，建造这个东西比给它拍照有趣多了。[Matthew Millman]花了近十年的时间，将他多年来所学的一切结合起来，最终[记录了他的开源智能风扇控制器](http://www.mattmillman.com/projects/another-intelligent-4-wire-fan-speed-controller/)的最终版本，但看看最终的结果，我们很高兴他做到了。

这块板的核心是一个 ATmega328P，但不要叫它 Arduino。[Matthew]说得很清楚，如果你想破解这个项目的代码，你不仅需要有一个针对所述芯片的程序员，还需要了解 AVR-GCC。他为这些内容提供了预构建的二进制文件，以默认设置运行，[，但你仍然需要自己将它闪存到芯片上](https://hackaday.com/2010/10/25/avr-programming-02-the-hardware/)。该项目旨在使用常见的 DS18B20 温度传感器，作为额外的奖励，固件[甚至可以检查你的是否是盗版](https://hackaday.com/2017/12/27/a-guidebook-to-the-world-of-counterfeit-parts/)(剧透:很有可能是)。

可以说这个风扇控制器最有趣的特性是它的命令行界面。只需插入板上的串行端口，打开终端仿真器，您就可以使用一组简洁的功能来查询传感器以及设置风扇的温度阈值和 RPM 范围。甚至有一个内置的“帮助”功能，如果你忘记了一个命令或适当的语法。

最初[Matthew]开发这个项目是为了控制一个电脑机箱内的多个风扇，但是很自然地，[事情与早期的](https://hackaday.com/2010/03/03/led-and-fan-controller/)相比发生了很大的变化。虽然今天不缺少可以根据钻机内部温度控制一系列风扇的花哨控制器，但还是有必要推出自己的解决方案。更重要的是，完全开源的可编程风扇控制器肯定还有其他潜在用途[。](https://hackaday.com/2018/09/11/temperature-controlled-fan-keeps-printer-cool/)