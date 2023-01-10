# 为四线测量创建开尔文测试引线

> 原文：<https://hackaday.com/2020/08/28/creating-kelvin-test-leads-for-four-wire-measurments/>

[VoltLog]有一个便宜的汉特 LCR 测量仪，但它只有两个探头。不过，最好的电阻和阻抗测量使用四线来提高精度。第一个订单是一个[定制的 PCB](https://github.com/voltlog/kelvin-leads) ,用于安装仪表的连接器，以及一个 3D 打印的外壳。

使用四线方案需要不寻常的鳄鱼夹，这种鳄鱼夹不会将钳夹短接在一起。夹子很难焊接，更难消除应力。但是[VoltLog]似乎处理起来没什么问题。

当然，有一些现成的解决方案，但是好的并不便宜。此外，这样，铅的长度正是你想要的，你可以控制整个建设，包括屏蔽和应变释放。

如果你以前没有遇到过四线检测，这是一个简单的想法。在正常的双线测量中，通过被测设备发送一个电压，然后测量通过导线的电流。但是，由于您使用同一对导线来传输和测量电流，测试引线的电阻会在测量中纠缠在一起。

有四根导线时，一对导线用来提供电流，另一对用来测量两端的电压降。传感线不会承载太多的电流，因此，在被测设备和测量设备之间不会有显著的电压降。电源线上可能会有压降，但我们已经不在乎了。

我们已经在许多不同的地方[看到了四线测量](https://hackaday.com/tag/four-wire-sensing/)。我们甚至[模拟了它如何改进测量](https://hackaday.com/2019/06/05/circuit-vr-resistance-measurement-with-four-wires/)，你也可以。

 [https://www.youtube.com/embed/MpJgCks37lE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MpJgCks37lE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

