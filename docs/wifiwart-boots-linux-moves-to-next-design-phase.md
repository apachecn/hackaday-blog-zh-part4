# WiFiWart 启动 Linux，进入下一个设计阶段

> 原文：<https://hackaday.com/2021/07/26/wifiwart-boots-linux-moves-to-next-design-phase/>

在过去的几个月里，我们一直在关注 WiFiWart，这是一个雄心勃勃的项目，旨在开发一款小到足以装入 USB 壁式充电器的 Linux 单板计算机(SBC)。开发者[Walker]表示，目标是为渗透测试创建一个容易隐藏的“投件箱”，让安全研究人员在目标网络中有一个宝贵的立足点，从那里进行侦察或发起攻击。当然，我们不需要告诉 Hackaday 的读者，你可以用这么小的开放硬件 Linux SBC 做很多其他的事情。

[![](img/b0e0667e79225b7a9c1cbea894cff9b8.png)](https://hackaday.com/wp-content/uploads/2021/07/wifiwart3_detail.jpg) 今天我们很高兴地向大家报告[【沃克】已经获得了第一个可以引导到 Linux](https://machinehum.medium.com/im-putting-a-wifi-router-into-a-wall-charger-part-2-bf04c779c905) 的开发板版本，尽管正如你可能预料到的那样，考虑到这个复杂的项目，在这个过程中会遇到一些困难。从导致 U-Boot 抛出错误的*单个*缺失电阻到为嵌入式主板编译内核的细节，他写的关于他的进展的最新博客文章提供了关于从头开始创建 SBC 的有趣见解。

一旦开发板被引导进入 Linux，[Walker]就开始测试系统的不同方面。一项内存基准测试证实，挑剔的 DDR3 RAM 工作正常，他能够加载双 RTL8188 接口的内核模块并连接到网络。虽然这两个 WiFi 模块目前挂在电路板的全尺寸 USB 端口上，但它们最终将集成到 PCB 中。

至关重要的是，这种原型板还可以让[Walker]了解最终硬件的能耗情况。即使在完全倾斜的情况下，这个较大的板在 5 VDC 下也不会超过 500mA；因此，如果他设计最大输出为 1 A 的电源，他应该有一个不错的安全裕量。[正如上一篇文章](https://hackaday.com/2021/07/03/wifiwart-linux-pentesting-device-gets-first-pcbs/)中提到的，目前的计划是将 PSU 放在自己的板上，这将允许更有效地利用充电器的内部体积。

随着软件和硬件现在在很大程度上被锁定，[Walker]说他的注意力将转向让一切都足够小，以适应最终的形状因素。这无疑将是该项目的最具挑战性的方面，但随着越来越多的黑客和工程师社区为这项事业贡献他们的专业知识，我们相信 WiFiWart 很快就会成为现实。