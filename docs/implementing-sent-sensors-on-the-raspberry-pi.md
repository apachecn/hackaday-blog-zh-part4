# 在 Raspberry Pi 上实现 SENT 传感器

> 原文：<https://hackaday.com/2020/12/22/implementing-sent-sensors-on-the-raspberry-pi/>

SENT 协议代表单边半字节传输，用于需要发送高分辨率数据同时保持低系统成本的传感器。它最常用于汽车领域，可以在诸如线控油门踏板和温度传感器等部件中找到。[【马克·史密斯】着手研究他是否能在不使用中间微控制器的情况下让圆周率零点读取这些传感器。](https://surfncircuits.com/2020/11/27/implementing-a-single-edge-nibble-transmission-sent-protocol-in-python-for-the-raspberry-pi-zero/)

[Mark]最初的尝试依赖于 Python 和 RPI。GPIO 库。不幸的是，引入的开销使得解码发送的流量成为不可能。[Mark]没有被吓倒，继续工作，利用了`pigpio`库及其回调函数，该函数允许以高达 1 微秒的速度采样。这足以从使用该协议的 LX3302A 电感式位置传感器读取信息。

对于那些试图使用某些传感器的人来说，这个项目可能会证明是有用的，他们希望避免给 Raspberry Pi 项目增加复杂性。好奇的人可以在 Github 上找到文件。我们以前也见过其他直接使用 Pi 构建的传感器——[,比如这个电源监控系统](https://hackaday.com/2020/07/24/a-complete-raspberry-pi-power-monitoring-system/)。休息后的视频。

[https://videopress.com/embed/KlDffRHE?hd=1](https://videopress.com/embed/KlDffRHE?hd=1)