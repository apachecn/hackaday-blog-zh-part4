# 用于动物网络的微型 GPS 记录器

> 原文：<https://hackaday.com/2022/09/18/tiny-gps-logger-for-the-internet-of-animals/>

[Trichl]创造了一个名为“tick tag”的微型 GPS 记录器，作为动物研究的廉价位置跟踪选项。LiPo 电池的低成本、小尺寸和大功率密度使其能够跟踪大量小动物，包括狗和蝙蝠。

TickTag 能够从其 30 毫安时的电池中获得 10，000 次 GPS 定位。每个单元都配有一个由 Atmel ATtiny1626 微控制器控制的 L70B-M39 GPS 模块，并配有一个微型 AXE610124 10 引脚连接头，用于编程和通信。GPS 数据存储在一个 128 kB 的 EEPROM 芯片上，每个 GPS 定位使用 25 位纬度、26 位经度和 29 位时间戳。将所有这些加起来，您会得到每个 GPS 数据点 10 个字节(25+26+29=80)，给出 10k GPS 定位的上限。

为了记录更高质量的数据并延长电池寿命，TickTag 可以编程为使用可变频率间隔或在越过地理围栏界限时记录 GPS 位置数据。

由于该设备非常小，任何靠近天线的错误信号都会导致接收问题。[Trichl]警告说，在安装设备时，它应该远离任何其他标签或导电材料，包括它自己的电池，电池需要安装在标签后面，而不是下面，以避免淹没 GPS 信号。

![TickTag connected to a User Interface Board](img/7eacb336be9ca29a4579b7f770c757e2.png)

从 TickTag 中获取数据需要对设备进行物理访问，这可以通过一个配套的“用户界面板”来完成。接口板集成了充电逻辑和 USB 通信等功能，降低了 TickTag 模块本身的复杂性。

源代码、Gerbers、设计文件和 3D 可打印案例可在 [GitHub](https://github.com/trichl/TickTagOpenSource) 上获得。除了文档和源代码，[他们在公共科学图书馆(PLOS 一号)期刊上的论文](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0267730)充满了细节，包括在家犬身上植入设备的结果。

谁知道呢，也许 TickTag 甚至有足够的弹性来追踪家猫。