# 从旧分光光度计中获取串行数据

> 原文：<https://hackaday.com/2022/06/25/getting-serial-data-out-of-an-old-spectrophotometer/>

[Jure Spiler]拥有一台旧的分光光度计，用于测量样品中光的吸收率和透射率。从设备中获取数据很困难，特别是当问题中的模型是缺少一些功能的教育版本时。然而，锲而不舍的努力让这台旧机器愉快地与电脑对话。

在早期的实验中，[嗅出发送到 LCD](https://hackaday.com/2022/05/05/exporting-data-from-old-gear-through-lcd-sniffing/) 的信号后，【Jure】做了更多的研究。原来，[一种特殊的昂贵电缆](https://www.fishersci.fi/store/products/spreadsheet-interface-software-exports-result/11380392)可以连接到设备的并行端口并传输串行数据，€的价格为 356 欧元。现在知道串行输出存在，[Jure]就能够找到所需的数据流。

将逻辑分析仪连接到机器上的“并行端口”上，可以发现该设备实际上会通过端口上的某些引脚发送串行数据。更难的是，它是反向 RS232 形式的。因此，只需将一个简单的 TTL 反相器连接到 USB-TTL 适配器上，就可以让该设备与现代 PC 通信。

完成后，[Jure]能够快速编写一个简单的 VB6 程序，从光谱仪中收集数据，并将其放入 CSV 文件中以供进一步分析。甚至有一个程序可以立即绘制数据图表，使科学仪器比以往任何时候都更容易和更快地使用！

通常，像这样的老科学硬件并不特别难破解。这通常很难让忙碌的科学家们掏钱购买花哨的适配器和电缆，而不是专业黑客的对手！