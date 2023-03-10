# 倾听你周围的射频

> 原文：<https://hackaday.com/2021/06/27/listen-to-the-rf-around-you/>

如今，对于用于 RF 分析的 SDR，我们有很多选择，但有时我们更感兴趣的是 RF 源，而不是传输内容。为了这个角色，[Drew]创造了 [RFListener](https://www.wolfsprojectfiles.com/projects/rflistener.php) ，一种将电磁信号转换为音频的宽带定向 RF 接收器。

RF 监听器围绕 AD8318 解调器分线板构建，利用定向宽带(900 Mhz–12 Ghz)PCB 天线接收信号，并输出模拟信号。该信号通过一系列放大器和滤波器产生音频，然后输入车载扬声器。一切都装在一个模糊的手枪形状的外壳中，背面有一些开关和一个 LED 振幅指示器。[Drew]在他的房子周围演示 RFListener，将它指向各种设备，如他的路由器、婴儿监视器和微波炉。在某些情况下，如玩具无人机，调制频率太高，无法产生音频，因此 RF 监听器也可以切换到“音调模式”，输出与信号幅度成比例的音频音调。

该电路完全是模拟的，设计首先在 [Falstad 电路模拟器](https://hackaday.com/2021/06/11/circuit-vr-arduino-virtually-meets-analog/)中完成，随后是一些试验板原型，以及用于最终版本的定制 PCB。事实上，这已经是一个有趣的探索设备，但如果有可能调整接收器的带宽和频率，将其变成宽带[猎狐](https://hackaday.com/2020/12/26/fox-hunting-with-software-defined-radio/)工具，那就更有趣了。