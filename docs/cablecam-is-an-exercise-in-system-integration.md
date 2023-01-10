# Cablecam 是系统集成的一个练习

> 原文：<https://hackaday.com/2021/08/04/cablecam-is-an-exercise-in-system-integration/>

无人机已经成为移动航空相机平台的标准，但在专业领域使用的另一种选择是电缆相机。作为整合机械、电子和软件的一项练习，[maxipalay]创造了他自己的 [Cablecam](https://hackaday.io/project/180869-cablecam) 。

Cablecam 是围绕一对加工过的木板建造的，在它们之间有一些滑轮和电机减速齿轮。一个无刷的业余爱好电机沿着绳索/电缆移动平台，驱动无人机 ESC。由于电子稳定控制系统没有反转功能，[maxipalay]使用了四个由 Arduino 控制的继电器来交换两条电机电线的连接，以反转方向。主机载控制器是一个 Raspberry Pi，连接到安装在双轴万向节上的相机模块以实现稳定。还增加了 GPS 模块，用于定位长电缆上的信息。

该基站是围绕一个 Nvidia Jetson Nano 建立的，连接到一个安装在塑料外壳中的 7 英寸屏幕。视频、遥测和控制信号使用开源 [Wifibroadcast](https://github.com/svpcom/wifibroadcast) 协议进行通信。这在无连接模式下使用现成的 WiFi 硬件来广播 UDP 数据包，并避免每次连接中断时冗长的 WiFi 重新连接过程。Cablecam 的运动可以使用控制站上的电位计手动控制，或者使用 Jetson 的机器视觉功能自动跟踪和跟随人。

这些年来，我们已经看到了几个电缆机器人，包括一个类似树懒的太阳能传感器平台[。](https://hackaday.com/2020/07/05/slothbot-lives-up-to-its-name/)