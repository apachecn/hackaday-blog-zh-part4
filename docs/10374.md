# 一款大型模块化智能手表，满足您的科幻幻想

> 原文：<https://hackaday.com/2021/06/11/a-massive-modular-smartwatch-to-match-your-sci-fi-fantasies/>

现代智能手表有一些令人难以置信的功能，但它们仍然没有科幻小说向我们承诺的那样，无论是尺寸还是功能。幸运的是，[扎克·弗里德曼]已经开始用[奇点管](https://hackaday.io/project/169343-singularitron-modular-cyberwatch)改变这种情况，这是一种模块化的可穿戴计算机，不像苹果手表，更像 Pip-Boy。

这个庞然大物最引人注目的特征是它的尺寸和停产的[四线 VFD 显示器](https://hackaday.com/2009/07/13/parts-4x20-vfd-character-display-na204sd02/)。输入由一排大的 RGB 照明按钮和一个旋转编码器组成，旋转编码器以一定角度安装在佩戴者的手臂上。内部是一对 PCB，集成了 Teensy 3.2、BLE 模块、运动处理模块、触觉驱动器和从可拆卸的 18650 电池获取的电源电路。这个臂章来自一个商用的腕戴式条形码扫描仪，它通过一个快速分离的支架连接到奇点加速器上。

奇点管的一个主要特点是它的模块化。围绕其边缘排列的是四个插槽，带有用于附加模块的弹簧加载触点。模块可以访问 SPI 和 I2C 总线、两个 GPIO 引脚、3.3 V 和 5 V 线路。每个模块还包含一个 EEPROM 芯片，用于存储模块的 ID 和任何配置设置，允许模块热插拔和自动识别。[Zack]已经创建了许多模块，如激光笔、环境传感器、有机发光二极管显示器和使 LED 闪烁的 Teensy 4.0。当一个模块被插入时，一系列随机生成的状态信息会在显示屏上闪烁，这要归功于一个[很棒的小库](https://github.com/ZackFreedman/Singularitron/blob/master/SingularitronFirmware/flavortext.h)，我们绝对是在为自己的项目复制这个库。具有讽刺意味的是，保持时间是 Singularitron 的弱点之一，因为[Zack]无法在里面安装备用电池，所以当电池耗尽时，时间需要重置。也许带 RTC 和备用电池的模块是完美的解决方案。

Singularitron 是[Zack]最初的[智能手表](https://hackaday.com/2014/07/19/wearable/)的升级版，它有着同样厚重的美感。他的其他项目是 Hackaday 上的一个常规功能，包括从 [Nerf 狙击步枪](https://hackaday.com/2021/04/15/3d-printing-a-long-range-nerf-blaster/)到[头戴式眼球跟踪器](https://hackaday.com/2020/10/02/seek-and-ye-shall-command/)的一切。

 [https://www.youtube.com/embed/sxfJOMjZeIs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sxfJOMjZeIs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

