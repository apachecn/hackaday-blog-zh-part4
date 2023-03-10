# 把廉价 WiFi 模块变成廉价 WiFi 瑞士军刀

> 原文：<https://hackaday.com/2018/08/17/turning-cheap-wifi-modules-into-cheap-wifi-swiss-army-knives/>

当 ESP8266 发布时，它是作为一种简单的设备出售的，可以通过 UART 连接到 WiFi 网络。它实际上是任何微控制器的 WiFi 调制解调器，只需几美元。这本身就很棒，但是后来黑客们得到了它。事实证明，ESP8266 实际上也是一个非常强大的微控制器，最新的模块有大量的闪存和引脚，可用于所有嵌入式项目。

为了让[Amine]获得黑客日大奖，他将 ESP8266 用作终极 WiFi 瑞士军刀。Kortex Xttend Lite 是一个非常小的 WiFi 中继器，它能够通过 WiFi 网络做任何事情，并且通过添加一点硬件，也可以连接到以太网。

该板上的硬件配备了一个 ESP8266-07S 模块，带有两个用于多种功能的空闲 GPIO 引脚。那里有一个 USB 转 UART，还有一个电压调节器，能够为稍微耗电的收音机输出 600 毫安的电流。还有一个集成的电池管理和充电控制器，允许该板为现成的锂电池充电，并在没有任何电线的情况下运行数小时。

那么，这个板子能做什么呢？一把小小的 WiFi 瑞士军刀，应有尽有。有流量整形、端口映射、数据包嗅探，甚至支持网状网络。上面还有一个 SMA 连接器，所以带上你的水壶——这也是扩展 WiFi 网络的一个好方法。

这是一个精心设计和执行的项目，更令人惊奇的是，这是作为[Amine]的高中项目之一完成的。是的，完成这个项目花了大约一年的时间，但对于[Amine]的第一个“高复杂性”设计来说，这仍然是一项了不起的工作。这使它成为一次极好的学习经历，也是今年 Hackaday 奖的绝佳参赛作品。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)