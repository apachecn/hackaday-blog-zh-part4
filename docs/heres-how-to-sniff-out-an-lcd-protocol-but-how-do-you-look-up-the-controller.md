# 这里是如何嗅出一个液晶协议，但你如何查找控制器？

> 原文：<https://hackaday.com/2021/07/30/heres-how-to-sniff-out-an-lcd-protocol-but-how-do-you-look-up-the-controller/>

没有什么比得到一个回收的组件来做你的投标感觉更好了。但在电子显示器领域，这一过程很快就会陷入困境。对于更复杂的显示器来说，仅仅是让这些东西打开所必需的秘密咒语可能是行不通的。今天的练习目标是一个简单得多的字符显示，还有一个额外的好处是[能够从一个正常工作的无线电单元](http://trochilidae.blogspot.com/2021/07/reverse-engineering-lcd-display-i-have.html)中嗅探数据。

当[阿门]升级他的 DAB 收音机时，他注意到了 16×2 字符显示器。显示器和控制器之间有三条走线，使用示波器很快就能追踪出两条数据线。图灵在示波器上的解码功能证实了他的预感，即示波器使用了 I2C，并给他提供了大量的数据。这包括一个设备地址，初始化字符串，每个字符都是用数据总线上的两个字节画在屏幕上的。

他说，一些搜索找到了最有可能的硬件:一个 Winstar WO1602I-TFH- AT 衍生自 ST7032 控制器。我们想知道的是，是否有搜索这类信息的好资源？我们的目标是[LCD 显示器和控制器参考](https://hackaday.com/2021/03/20/a-handy-reference-for-display-drivers-and-lcd-controllers/),我们在三月份已经讨论过了。这是一个很好的资源，但是在这个特别的展示中出现了 bupkis。我们是否应该使用 DuckDuckGo 来初始化字符串，并希望过去有人发布过这些部分的驱动程序或逻辑转储，或者有更好的方法来实现这一点？请在评论中告诉我们！