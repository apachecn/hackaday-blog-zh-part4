# 垃圾桶的网卡-80

> 原文：<https://hackaday.com/2019/02/11/a-network-card-for-the-trash-80/>

围绕这些部分，[彼得]是众所周知的滥用 TRS-80 做的事情，它永远不应该做的。你可以在 TRS-80 上阅读维基百科，你可以看谷歌图片，你可以浏览网页。与任何逆向计算机一样，您可以做的事情也有限制。为了浏览维基百科，[Peter]必须建立一个 AWS 实例来翻译所有内容，并使用串行到 IP 转换器。可以做到，但是很难。

现在，在看到围绕 ESP32 构建的一些有趣的项目后，[Peter][为 TRS-80](http://pski.net/2019/02/03/trsnic/)构建了一个网卡。它被称为 trsnic，是几乎所有 TRS-80 的工作网卡，最终目标是支持 TRS-80 I/II/III/4/12/16/16B 和 6000。

trsnic 的想法来自[Arno Puder]的[retro store card](https://github.com/apuder/RetroStoreCard)，这是一种插入 TRS-80 Model III 并将其连接到各种“个人云”的设备，无需磁带或软盘即可托管和运行应用程序。它通过连接到 Model III 中 I/O 总线的 ESP32 来实现这一点，并且这一切都是完全开源的。

[Peter]采纳了这个想法并付诸实施。由于在 ESP32 中发现的能力，真正的加密互联网通信可以发生，这意味着 HTTPS 和 TLS。

目前，trsnic 的文档是有限的，但该项目确实存在，构建它就像在 PCB 中填充一些接头和 DIP 插座并焊接它们一样简单。在 ESP32 代码上有一些工作要做，但是如果你正在为你的 Trash-80 寻找一个网卡，这是现在工作的一个。