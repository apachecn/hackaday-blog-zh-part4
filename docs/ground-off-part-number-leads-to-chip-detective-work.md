# 磨掉零件号导致芯片检测工作

> 原文：<https://hackaday.com/2020/12/06/ground-off-part-number-leads-to-chip-detective-work/>

有时，当一件电子产品落在工作台上时，你会发现它的芯片上的标记被磨掉了。制造商试图让逆向工程师的任务变得不那么容易，从而保护他们的市场。[Maurizio Butti] [在为远程控制系统设计的电子开关](https://ydiaeresis.wordpress.com/2020/11/26/switching-to-a-better-firmware/)中发现了一个意想不到的功能，它的简单工作是监听来自模型飞机或类似设备中接收器的 PWM 信号，并打开或关闭 FET。

根据以前的经验，他根据电源、接地、Rx 和 Tx 引脚的位置怀疑这可能是 STC 的微控制器。这个兼容 8051 的设备很容易被重新编程，所以他能够为它创建自己的固件。[他发布了代码](https://bitbucket.org/buttim/rcswitch/src/master/RCSwitch.c)，它非常简单，因为它只是复制了原始代码。他承认这可能看起来很奇怪，但他指出，这是为未来的升级留有余地，例如在闪光灯中重复循环输出。

除了他们早期的产品之外，我们在这里没有看到太多的 STC 芯片，但是 8051 核心在这里更有规律，因为它在 Nordic 的 NRF24 系列无线芯片中可以找到。