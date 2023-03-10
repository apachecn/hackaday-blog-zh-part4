# 你从来不知道你想要避免的 USB-C 连接器

> 原文：<https://hackaday.com/2022/02/20/the-usb-c-connectors-you-never-knew-you-wanted-to-avoid/>

在科技 Twitter 上，一些人因他们的事情而闻名——例如，[A13 (@sad_electronics)](当他们不忙着设计电子产品时)，在网上搜索以找到令人惊叹的优秀零件。他们找到的零件中有很大一部分因为所有错误的原因而变得杰出。今天那是一个[通孔两针 USB Type-C 插座](https://twitter.com/sad_electronics/status/1494666768517844993)。观察我们从中国(或英国)得到的廉价技术！)，你可能会得出结论，两个 5.1K 下拉电阻很难添加到一个产品中——这个插座使它几乎不可能。

我们以前见过两针 THT 微型 USB 插座，有时用于业余爱好者的工具包。然而，这一点违背了 C 类连接器的主要要求——吸(C 类供电)器件在 CC 引脚上具有下拉电阻，源器件(PSU 和主机端口)在 VBUS 上具有上拉电阻。正如反汇编所示，这个连接器既没有这些功能，也不能让您添加任何东西，因为 CC 引脚实际上是不存在的。如果您使用此端口制作 USB-C 供电的设备，符合 Type-C 标准的 PSU 不会为其供电。如果你试图用它做一个 C 型 PSU，一个兼容的设备应该(理所当然！)拒绝从中收费。这个端口的唯一好处是当使用它的设备与 USB-A 到 USB-C 电缆捆绑在一起时——积极地阻碍 Type-C 连接器取得的任何进展。

尽管 USB Type-C 的基本原理很简单，但制造商经常会弄错——回到 2016 年，一根错误的电缆可能会[毁掉你 1.5k 美元的 MacBook](https://hackaday.com/2016/02/04/the-usb-type-c-cable-that-will-break-your-computer/) 。如今，我们可能只需要偶尔用一对 5.1K 电阻来修改器件。我们只能希望[新的欧盟法律](https://hackaday.com/2021/10/12/showdown-time-for-non-standard-chargers-in-europe/)将迫使设备得到它的权利，并停止破坏每个人的便利，所以我们可以[最终享受承诺给我们的东西](https://hackaday.com/2020/06/23/usb-c-is-taking-over-when-exactly/)。黑客已经制造出越来越多带有 USB-C 端口的设备，甚至到处改装 iPhones。如果你想进入恶作剧领域，滥用新技术的扩展功能，你甚至可以制作一个设备，如果你翻转电缆[以不同方式列举](https://hackaday.com/2021/03/22/cursed-usb-c-when-plug-orientation-matters/)，或者制作一个“FPC 上的 BGA”加密狗[，它完全隐藏在 C 型电缆末端](https://hackaday.com/2022/01/01/genius-or-cursed-this-usb-c-connector-is-flexible/)内！