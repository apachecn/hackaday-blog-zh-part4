# ZeroBug:从模拟到平稳行走

> 原文：<https://hackaday.com/2021/07/21/zerobug-from-simulation-to-smooth-walking/>

由于 3D 打印和廉价的业余爱好伺服系统，建造自己的小型行走机器人并不特别困难，但让它们平稳行走可能是一个完全不同的故事。从经验中了解到这一点，[Max。K]首先解决了软件方面的问题，在建造它之前，创建了他的 [ZeroBug 六足机器人](https://hackaday.io/project/180534-zerobug-diy-hexapod-robot)的虚拟模拟。

ZeroBug 从他以前制造四足动物的经验中学习，在[中以简单的简笔画](https://hackaday.com/2015/11/15/processing-for-raspberry-pi/)开始生活，随着【Max】逐渐增加复杂性。K]想出了让它正常行走的方法。他首先为每条腿的尖端开发了所需的运动序列，然后添加了关节，并使用反向运动学计算了致动器的运动。利用模拟的结果，他设计了机械装置，并将其拉回到模拟中进行最终验证。

每条腿使用三个微伺服系统，由定制 PCB 上的 STM32F103 控制，处理所有的运动计算。它通过 UART 从运行在 Raspberry Pi Zero 上的 python 脚本接收命令。这允许用户使用 WiFi 控制网络界面，或者使用蓝牙连接从游戏手柄控制。[Max。K]还在前面增加了一个钳子，让它能够与环境互动。休息后的视频。

最终的产品比我们见过的大多数其他伺服驱动的六足机器人移动更加平稳，整个项目都有很好的记录。电子设备和软件可以在 [GitHub](https://github.com/CoretechR/ZeroBug) 上获得，机械设备可以在 [Thingiverse](https://www.thingiverse.com/thing:4894719) 上获得。

The [HackadayPrize2021](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)

 [https://www.youtube.com/embed/rt-FT-M5G7A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rt-FT-M5G7A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

