# 改进的热变色时钟使用 PCB 加热器以获得更好的对比度

> 原文：<https://hackaday.com/2022/01/04/improved-thermochromic-clock-uses-pcb-heaters-for-better-contrast/>

我们喜欢围绕这些部分的时钟项目，所以这里我们有另一个不寻常的 7 段时钟设计。Hackaday 自己的[Moritz Sivers]对他上一个热变色时钟并不完全满意，[所以他离开并建造了另一个](https://www.instructables.com/Thermochromic-Clock-Frame-Version/)，解决了一些问题，这次他将它设计成壁挂式。[最初的设计](https://hackaday.com/2021/06/17/using-heaters-to-display-time/)有一个单独的加热器 PCB，使用分立电阻作为加热元件。这意味着来自有源元件的热量扩散到邻近区域，降低了对比度，使它有点难以阅读，但它看起来真的很酷。

这种新版本省却了电阻器，使用带有加热器走线的单个分段形状的 PCB，这使得该分段具有更均匀的热量，并且限制了热量向相邻的不活跃的气隙分段的泄漏。控制是通过同一个 [Wemos D1 迷你](https://www.wemos.cc/en/latest/d1/d1_mini.html) ESP8266 模块，驱动一系列 74HC595 移位寄存器和一堆双 NMOS 晶体管。DS18B20 温度计允许固件根据环境温度进行调整，使颜色变化效果更加一致。所有这些都被包裹在一个铝制框架中，如果你问我们，结果看起来非常好。

PCB 设计和 Arduino 固件都可以在 [project GitHub](https://github.com/vonsivers/Thermochromic-Clock-Frame) 上找到，所以对于那些有此倾向的人来说，复制这些应该足够简单，只要确保你的电源能够处理至少 3 安培，因为这些加热器肯定是耗电的！

有一个非常好的时钟，但迫切需要一个热变色温度/湿度显示器？[【莫里茨】你报道过](https://hackaday.com/2019/08/19/the-thermochromic-display-you-didnt-know-you-needed/)吗？如果这个数字钟太简单，那么用[一个 mad 1024 元件模拟热变色时钟代替](https://hackaday.com/2020/05/24/matrix-of-resistors-forms-the-hot-hands-behind-this-thermochromic-analog-clock/)怎么样？

 [https://www.youtube.com/embed/_qPiGKsSZ5w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=148&wmode=transparent](https://www.youtube.com/embed/_qPiGKsSZ5w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=148&wmode=transparent)

