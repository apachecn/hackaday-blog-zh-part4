# 具有现成硬件的 LoRa 网状网络

> 原文：<https://hackaday.com/2020/02/26/lora-mesh-network-with-off-the-shelf-hardware/>

网状网络的理想应用是离网通信；当没有蜂窝接收和 WiFi 无法到达时，LoRa 等广域技术可用于创建临时无线网络。无论你是与朋友一起享受户外活动还是进行救援行动，一个便宜的小工具将允许你创建这样的网络并通过它进行通信，这将是一个非常受欢迎的补充。

[这正是 Meshtastic 项目](https://www.meshtastic.org/)的目标，该项目旨在将现成的 ESP32 LoRa 开发板转化为价格合理的网状网络通信器。你需要做的就是买一个支持的板，安装固件，并开始啮合。[一款允许你使用网状网络](https://github.com/geeksville/Meshtastic-Android)发送基本文本信息的 Android 应用程序现已推出 alpha 版本，最终你将能够通过 LoRa 链接运行信号。

[![](img/64313f20a2dd7029762ae5da0b9c3d01.png)](https://hackaday.com/wp-content/uploads/2020/02/espmesh_detail.jpg)

Navigating to another node in the network.

开发人员 Kevin Hester 告诉我们，现在仍然是非常早期的阶段，还有大量的工作要做。事实上，他正在积极寻找一些志同道合的人加入这个项目。因此，如果你有 ESP32 或移动应用程序开发的经验，并且通过远程无线网络进行私人通信听起来像是你喜欢的聚会，这可能是你的幸运日。

从用户的角度来看，这个项目非常平易近人。除了为您的特定主板 3D 打印外壳之外，您不需要将任何定制硬件放在一起。第一次你需要用`esptool.py`刷新固件，但之后，【Kevin】说未来的更新可以由智能手机应用程序来处理。

顺便说一句，这两种主板的主要区别在于，更大、更贵的主板包含 GPS。网状网络方面的东西可以与任何一种板一起工作，但如果你的团队中的每个人都有配备 GPS 的版本，每个用户都可以看到网络中其他人的位置。

这[不是我们第一次看到 LoRa 被用来建立离网通信](https://hackaday.com/2019/03/24/custom-lora-pager-designed-with-care/)，当然也不会是最后一次。这项技术非常适合在没有任何现有基础设施的地方让设备进行通话，我们很高兴看到更多这方面的例子。