# 一个开放的硬件橡胶鸭子

> 原文：<https://hackaday.com/2019/07/24/an-open-hardware-rubber-ducky/>

不，这不是 Bert 最喜欢的 bathtime 玩具的开源版本(不过说真的，如果你看到了，请告诉我们)，由[Radik Bechmetov]开发的 [PocketAdmin 旨在成为 Hak5 中众所周知的“USB Rubber Ducky”](https://hackaday.io/project/165926-pocketadmin)渗透测试工具的替代产品。它可能看起来像一个标准的 USB 闪存驱动器，但在黑色塑料外壳下是一大堆数字恶作剧等待溢出。

[![](img/f57104722e87d45101841f38db7ac781.png)](https://hackaday.com/wp-content/uploads/2019/07/oshducky_thumb.jpg) 总的想法是 PocketAdmin 对于主机来说表现为 USB 人机接口设备(键盘、鼠标等)或者 USB 大容量存储设备。在这两种情况下，用户都有能力创建定制的有效负载，这些有效负载可以利用操作系统对本地连接设备的固有信任。最常见的例子是模仿一个 USB 键盘，一旦连接到电脑上就开始“打字”。

您甚至可以配置 PocketAdmin 广告的供应商和产品 id，从而允许您更准确地欺骗各种设备。[Radik]包含了一些其他有趣的特性，比如根据检测到的操作系统启动不同有效负载的能力。这样，当它连接到一个 Linux 机器上时，就不会浪费时间去敲 Windows 命令了。

硬件被设计成尽可能容易和便宜地复制。重物由 STM32F072C8T6 微控制器完成，结合 W25Q256FVFG 32MiB 闪存芯片存储有效载荷。除此之外，BOM 主要由无源器件和一些明显的位组成，如公 USB 连接器。[Radik]甚至提供了一个链接，指向您可以在哪里购买外观令人信服的 USB“闪存驱动器”外壳。

我们在过去已经看到了低成本的 DIY 版本的 USB 橡皮鸭，但 PocketAdmin 很有趣，因为它似乎是在寻找这个项目的新突破，而不仅仅是复制已经完成的东西。随着 2019 年 Hackaday 奖的升温，这肯定会是一个值得关注的问题。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)