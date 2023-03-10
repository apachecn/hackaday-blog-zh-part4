# 构建您自己的并网逆变器

> 原文：<https://hackaday.com/2020/05/29/build-your-own-grid-tie-inverter/>

将 DC 转换成交流电的逆变器非常常见，一些汽车甚至有标准的交流插座供你插入你最喜欢的电器。然而，有一种特殊类型的逆变器称为并网逆变器，它不仅可以产生交流电，还可以通过交流电源插座注入交流电，与普通交流电源一起为其他设备供电。为什么？也许你想使用自己的发电机或太阳能。在某些情况下，如果你生产的电力超过了你消耗的电力，电力公司会付给你钱。也许你只是想知道你能做到。这似乎是[【fother by】建造](https://www.instructables.com/id/Grid-Tie-Inverter/)背后的动机，相当充实。

该装置只能处理大约 60 瓦的功率，但它可以完成你需要的所有功能:DC 到交流的转换以及相位和电压匹配。实际上，如果您不关心波形，仅仅将 DC 转换为交流几乎是微不足道的。但在这种情况下，您确实需要创建一个交流信号来匹配线路上已有的信号。

使用 STM32F407 板简化了项目，该板具有一些漂亮的高速 A/D 以及 TI H 桥板。另一个简化是使用变压器，因此逆变器只需产生 40V 电压。这是一个非同小可且有些危险的项目。然而，[fotherby]提供了很多细节和理论，所以即使你不想建造它，你也可能会喜欢看这个作品。

说到安全，该系统检测公用电压是否看起来不好，如果是，该系统关闭逆变器。这有助于防止孤岛现象——公用事业公司或电工认为电路不带电，但电压来自另一个来源。

总的来说，这是一个非常有趣的项目，尤其是如果你不经常和电力线打交道的话。显然，如果你想在北美做这个，你需要做一些修改。无论你在哪里，如果你尝试这样做，我们建议你查阅一些[安全指南](https://hackaday.com/2019/06/05/protect-yourself-and-your-project-while-working-with-mains-power/)。

 [https://www.youtube.com/embed/O2MSjKQU08Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/O2MSjKQU08Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

