# 分光计通过用激光束轰击样品来检测化学物质

> 原文：<https://hackaday.com/2022/02/19/spectrometer-detects-chemicals-by-zapping-samples-with-a-laser-beam/>

在 Hackaday，我们喜欢那些以专业设备的一小部分成本获得有用的实验室设备的项目。[Lorenz]，在高级修补方面，[建造了他自己的激光诱导击穿光谱仪器](https://www.youtube.com/watch?v=2C7Hajgg9nU)，或 LIBS，这是一个相当令人印象深刻的设备。LIBS 是一种分析物质以发现其化学成分的技术。基本上，这个想法是用强大的激光轰击样品，然后观察产生的等离子体小云，并测量它发出的波长。

[![A plot showing the spectrum of hematite](img/fd93eb530c63f226b588205a321d23f4.png)](https://hackaday.com/wp-content/uploads/2022/02/LIBS-Hematite-spectrum.jpg)

The spectrum of hematite (iron oxide), compared to that of pure iron

使用的激光[Lorenz]是从纹身去除机器中回收的 Nd:YAG 装置。它发出脉冲后，光电二极管检测到光并触发光谱仪，光谱仪由衍射光栅、几个透镜和镜子以及线性 CCD 传感器组成。光栅将入射光分成不同的成分，这些成分落在 CCD 上并触发其像素。STM32 Nucleo 板读出结果，并将其发送到 PC 进行进一步处理。

那个处理部分本身就是一个完整的项目。[洛伦兹]呼吁[g3gg0]，谁[软件，简化了分光计](https://www.g3gg0.de/wordpress/programming/a-homebrew-libs-software-written-in-c/)的操作。首先，它有助于仪器的校准。将检测器对准众所周知的光源，如激光或荧光灯，然后在生成的光谱图上选择预期的波长。然后，软件会自动计算正确的系数，将每个像素映射到特定的波长。

该软件还包含一个与化学元素相对应的光谱数据库:一旦你获得了一个未知样品的光谱，你可以将这些光谱叠加到结果图上，并试图找到匹配。由此产生的系统似乎工作得很好。氧化铁和氧化银的样品给出了与其组成成分的合理匹配。

我们以前见过其他类型的光谱仪:如果你只是想表征一个光源，看看这个基于 Raspberry Pi 的型号。如果你对化学分析感兴趣，你可能也想看看[这个开源拉曼光谱仪](https://hackaday.com/2020/05/12/open-source-raman-spectrometer-is-cheaper-but-not-cheap/)。

 [https://www.youtube.com/embed/2C7Hajgg9nU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2C7Hajgg9nU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

