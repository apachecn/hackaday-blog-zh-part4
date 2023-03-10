# PinePhone 获得 3D 打印机械键盘

> 原文：<https://hackaday.com/2020/12/03/pinephone-gets-3d-printed-mechanical-keyboard/>

你还记得智能手机有真正的物理键盘的时候吗？通过 SSH 在一些远程机器上使用命令行是轻而易举的事情，如果您愿意，甚至可以删除几行代码。但是现在你要么不得不拖着一个外接键盘，要么忍受每分钟在一块玻璃上敲几个字的痛苦。对我们来说听起来不像是进步。

从表面上看，[詹姆斯·威廉姆斯]也不这么认为。他设计了一个[物理键盘插件，可以扣在 PinePhone](https://www.thingiverse.com/thing:4662295) 的背面，提供适当的，尽管是精简的打字体验。这也不是重新利用的黑莓板；他创造了一个定制的机械键盘，由于树脂印刷的键帽和 Kailh 低剖面开关，它可以折叠成令人难以置信的小尺寸。除了手绘的传说之外，可以毫不夸张地说这是一个比许多人实际电脑上的键盘更好的键盘。

[![](img/f60aede53220b6f188910d38120b13d0.png)](https://hackaday.com/wp-content/uploads/2020/11/pinekb_detail.jpg) 除了 3D 打印框架和 Kailh 开关，还有一个 Arduino Pro 微型板载与手机通信。键盘没有使用 USB，而是用[线连接到 PinePhone](https://hackaday.com/2020/08/03/pinephone-gets-thermal-imaging-backpack/) 背面的 I2C 附件端口。听起来[James]在准备发布之前需要多一点时间来完善他的 QMK 版本，所以在你开始打印你自己的部分之前，你可能需要等一会儿。

那些关注 PinePhone 开发的人知道，据说有一个官方键盘附件正在开发中，但是当我们离移动 Linux 涅槃如此之近的时候，谁愿意等待呢？此外，我们怀疑它是否会像董事会(詹姆斯)所做的那样令人愉快。