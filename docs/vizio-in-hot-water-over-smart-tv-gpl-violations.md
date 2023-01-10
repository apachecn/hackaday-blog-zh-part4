# Vizio 因智能电视违反 GPL 而陷入困境

> 原文：<https://hackaday.com/2021/10/22/vizio-in-hot-water-over-smart-tv-gpl-violations/>

正如这个社区中的大多数人所知道的，现在市场上任何标榜为“智能”的消费产品都很有可能在幕后运行某种形式的 Linux。我们也敏锐地意识到，让公司在他们的产品中使用 Linux 和其他 GPL 许可软件时遵守他们的协议，即发布他们修改的源代码，并不总是像它应该的那样简单。

偶尔，这些不合规的公司会让一些人变得如此愤怒，以至于他们实际上试图对此做些什么，[这就是智能电视制造商 Vizio 目前发现自己的处境](http://sfconservancy.org/vizio)。软件自由保护协会(SFC)最近宣布，他们正在将总部位于加州尔湾的公司告上法庭，因为他们在开发 Linux 驱动的 SmartCast 电视固件时多次未能满足 GPL 的要求。除了 Linux 内核，SFC 还声称 Vizio 正在使用各种其他 GPL 和 LGPL 保护作品的修改版本，如`U-Boot`、`bash`、`gawk`、`tar`、`glibc`和`ffmpeg`。

[![](img/18923ad6e70f04f385ca666698f4fd1b.png)](https://hackaday.com/wp-content/uploads/2021/10/viziogpl_detail.png) 根据香港证监会的新闻稿，该集团并未寻求任何金钱赔偿。他们只是希望 Vizio 按照 GPL 做他们需要做的事情，并发布 SmartCast 源代码，他们希望这将允许为旧的 Vizio 智能电视开发类似 OpenWrt 的替代固件。这一点尤其重要，因为旧型号通常会停止接收更新，并且在许多情况下，将不再能够访问它们宣传能够支持的所有服务。显然，证监会希望这个案件作为更大的修理权辩论的一部分来看待[，考虑到我们看到的一些智能电视附带的糟糕固件，我们倾向于同意。](https://hackaday.com/2021/07/27/ftc-rules-on-right-to-repair/)

当然，我们过去也看到过类似的案例。但这一案件的独特之处在于，证监会并不代表被发现软件属于 Vizio smart cast 的开发商之一，他们实际上是原告。通过站在购买了包含 GPL 软件的 Vizio 产品的消费者的立场，SFC 被视为第三方受益人，他们只是要求法院根据许可证条款给予他们应得的东西。

作为开源运动的坚定信仰者，[我们绝不容忍违反许可的人](https://hackaday.com/2018/08/27/gpl-violations-cost-creality-a-us-distributor/)。Vizio 可不是什么天真的青少年，会随意抄袭他们从 GitHub 找到的代码，却不理解其中的含义。这是一家价值数十亿美元的公司，绝对应该更好地了解情况，我们很高兴看到他们在最终被迫遵守规则之前有所改变。