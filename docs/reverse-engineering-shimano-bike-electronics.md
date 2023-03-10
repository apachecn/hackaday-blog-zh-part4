# 逆向工程禧玛诺自行车电子

> 原文：<https://hackaday.com/2019/03/26/reverse-engineering-shimano-bike-electronics/>

ANT+是一种专门设计用于传感器的无线协议，在某些方面具有与蓝牙低能耗类似的功能。它在各种自行车设备制造商中找到了一席之地，可以连接智能手表、自行车电脑和电子换挡器。当然，一旦某样东西成为事实上的标准，就必须有人开始在界限之外着色。在这种情况下，Shimano 离开了他们的 DI2 组，[离开了[kwakeham]手头的逆向工程工作](https://www.youtube.com/watch?v=25Kyh5im_ak&feature=youtu.be)。

[kwakeham]为我们提供了一个如何进行逆向工程的很好的例子。通过 FCC ID 研究 Shimano 硬件表明，该设备使用 ANT+设备中常见的 NRF24AP2 芯片进行通信。然后打开 Shimano 器件，将逻辑分析仪连接到各个测试点，直到找到收发器和微控制器之间的 SPI 接口。在这一点上，这是一个简单的问题，把硬件通过它的步伐和捕捉数据，直到协议可以被拉出来，一块一块。

[这项工作记录在 Github](https://github.com/kwakeham/DiHack/wiki) 上，供任何希望与 Shimano DI2 groupset 互动的人使用。逆向工程是一项强大的技能，可以教会你从[口袋妖怪](https://hackaday.com/2019/01/04/pokemon-cries-and-how-they-work/)到[僵尸网络](https://hackaday.com/2018/09/09/source-of-evil-a-botnet-code-collection/)的一切。休息后的视频。

 [https://www.youtube.com/embed/25Kyh5im_ak?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/25Kyh5im_ak?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

