# DIY 按钮矩阵亮起并说出 I2C

> 原文：<https://hackaday.com/2019/05/17/diy-button-matrix-lights-up-and-speaks-i2c/>

[戴维·约翰逊-戴维斯]一直想要一个照明按钮矩阵的项目，但成本从来不是很友好。当他在全球速卖通上发现一种廉价的照明按钮来源时，这一切都改变了，导致了这种 DIY 4×4 照明按钮矩阵设计，它通过 I ² C 进行通信。按钮状态可以独立于灯光模式的设置进行读取，每当检测到变化时，可选的中断信号就会被拉低。对于一块 PCB 和价值 10 美元的组件来说，这已经不错了！

该设备使用 ATtiny88 上的每一个引脚，因为每个按钮都有自己的引脚，所以可以通过引脚变化中断来检测按键。I ² C 上按钮的状态报告是明确的，即使同时按下多个按钮。一个简单的协议提供了所有需要的功能，所有连接都被带到板的边缘，以允许容易地平铺多个面板。

[GitHub 储存库](https://github.com/technoblogy/illuminated-button-matrix)包含代码和 PCB 文件，【David】将电路板文件分享给[奥什公园](https://oshpark.com/shared_projects/qEsH0WZZ)和 [PCBWay](https://www.pcbway.com/project/shareproject/Illuminated_Button_Matrix.html) 以方便订购。此外，他提供了两个演示(Tacoyaki 和 Tacoyaki+)是与经典的[熄灯](https://hackaday.com/2013/02/18/a-beautiful-game-of-lights-out/)相关的游戏，以展示矩阵。