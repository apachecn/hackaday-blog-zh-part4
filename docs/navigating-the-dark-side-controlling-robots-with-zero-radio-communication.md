# 导航黑暗面:用零无线电通信控制机器人

> 原文：<https://hackaday.com/2019/10/20/navigating-the-dark-side-controlling-robots-with-zero-radio-communication/>

虽然自主机器人在过去一直是一些项目的主题，但这个特殊的项目试图建造一个可以教孩子们控制和机器人技术的机器人。

这个想法是模仿在月球黑暗面的太空任务，在那里无线电联系几乎是不可能的。学生们学习编程和调试嵌入式设备和传感器，甚至在他们中的一些人学会字母表之前！

挑战的[材料允许用简单的 Arduino 程序(Blink)以及 C++或 Java 等低级语言对微控制器进行编程。主要硬件包括一个基于 Arduino Uno R3 的漫游器，由 ESP8266 通过 WiFi 进行控制。机器人的传感器数据是从超声波距离传感器、摄像头以及 SIM7000E GSM+GPS 收集的。命令从服务器轮询，通过网页和 REST 接口发送。](https://gitlab.com/ecolefrancodanoise/arduino-efd/tree/master/darkside)

漫游者对指示方向的命令做出反应，拍摄照片，并远程扫描其距离。一些自定义库是为串行通信和相机编写的，以解决不稳定的通信。最新的挑战扩展是一个关注电池寿命和功耗的探测器，要求学生解释机器人一生中的功耗。

自项目构思以来，漫游者已经在学校使用，我们很高兴看到年轻学生学习控制和编程的新方法。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)