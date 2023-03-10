# 婴儿迈向 DIY 自动驾驶:大众高尔夫版

> 原文：<https://hackaday.com/2022/01/08/vw-power-steering-reverse-engineering/>

![](img/df54d6a8f702a1bc6712512fece3d011.png)

Nice thermal design, but conformal coating and no ID marks make this tough to reverse engineer

[Willem Melching]拥有一辆 2010 款大众高尔夫(在欧洲非常常见),他注意到虽然电子转向齿条支持通常的车道保持辅助(LKAS)系统，并且理论上能够使用`openpilot`在更高级的配置中运行，但大众的实施存在一些缺点，这意味着它不会运行足够长的时间来使其可行。[Willem]对逆向工程汽车 ECU 非常感兴趣，并且显然非常有能力将它们破解并使其屈服，[Willem]开始[记录他为自己的汽车](https://blog.willemmelching.nl/carhacking/2022/01/02/vw-part1/)解锁 openpilot 支持的旅程。

这是一次怎样的旅行！这个由四部分组成的博客系列写得很漂亮，展示了每一个血淋淋的细节和一路上使用的所有工具。第一部分显示了 2010 款大众高尔夫 Mk6 模块(位于三相转向齿条电机的背面)的电子动力转向(EPS) ECU，该模块被打开以展示一种有趣的多芯片模块方法，裸芯片直接粘合到一对基板 PCB，然后粘合到电机外壳的背面，可能是出于散热原因。聪明的设计，但令人沮丧的同时，这使得部分识别有些棘手！

![](img/f21aafb3b6ca345d0b210a1ba0a4373d.png)

Entropy less the 1.0, and zero sections indicate no encryption applied

[Willem]使用各种工具和技巧来启动和嗅探 CAN 总线上的 ECU 流量，当连接到符合 [SAE J2534-](https://www.kvaser.com/about-can/can-standards/j2534/) 的调试工具时，最终确定它使用[大众特定的 TP2.0](https://jazdw.net/tp20) CAN 总线协议，并设法获取足够的流量来检查是否可以使用标准的 KWP2000 诊断协议来访问一些有趣的数据。接下来是对网上找到的更新图像进行非常深入的逆向工程，首先进行一些琐碎的异或运算，然后使用 [Binwalk](https://www.kali.org/tools/binwalk/#:~:text=Binwalk%20is%20a%20tool%20for,for%20the%20Unix%20file%20utility.) 查看文件的熵图，以确定他是否真的有代码，如果是加密的，在运行 [cpu_rec](https://github.com/airbus-seclab/cpu_rec) 后，确定 cpu 是[瑞萨 V850](https://www.renesas.com/eu/en/document/mah/v850-familytm-architecture?language=en) 。然后真正的工作开始了——将图像加载到 Ghidra 中，开始猜测代码的架构，找出需要修补的地方，以进行所需的更改。在该系列的最后一部分，[Willem]提取并使用引导加载程序来部分修补他的车辆的代码配置区域，并解锁他所瞄准的目标-远程控制他的转向。(好吧，真正的目标是运行 [openpilot。](https://github.com/commaai/openpilot))

在我们看来，这是一个非常有趣的，如果长，阅读显示一个迷人的主题熟练地执行。但我们想强调的是，车载 EPS 模块是一个经过 [ASIL-D 安全测试的](https://en.wikipedia.org/wiki/Automotive_Safety_Integrity_Level#ASIL_D)设备，所以如果在索赔事件中被发现，你对公路行驶车辆的任何攻击肯定会使你的保险无效(更不用说你的保修了)。

如果你能调用 EPROM 的话，老式的 ECU 就更容易被黑客攻击了，而外面的人[正在为各种各样的车辆黑客攻击](https://hackaday.com/2021/04/25/small-open-source-vehicle-hacking-platform/)生产模块。有这么多可修补的！