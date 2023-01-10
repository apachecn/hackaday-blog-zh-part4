# DIY 橡胶鸭子和它的名字一样便宜

> 原文：<https://hackaday.com/2018/09/17/diy-rubber-ducky-is-as-cheap-as-its-namesake/>

Hak5 的“橡胶鸭子”是一个非常强大的工具，可以让用户执行快速击键注入攻击，这基本上是一种花哨的说法，即该设备可以快速打字。Mavis Beacon 能够以超过 1000 WPM 的速度输入文本，但在这个 45 美元的小工具上却一无所获。在插入的短短几秒钟内，一个正确编程的脚本可以造成各种破坏。想象一下攻击者在本地机器上输入命令会造成多大的破坏，现在想象一下它们也是 Flash。

但是除非你是一个专业的圣灵降临者，否则 45 美元可能会比你想花的要多一点。幸运的是，对于那些有预算意识的黑客来说，[【托马斯·C】已经发布了一个使用开源软件的指南，以 3 美元一个](https://medium.com/@tomac/low-cost-usb-rubber-ducky-pen-test-tool-for-3-using-digispark-and-duck2spark-5d59afc1910)的价格创建一个 Hak5 工具的 DIY 版本。以这样的成本，当您部署它们时，您甚至不必费心去恢复它们；抓紧你的头套[然后逃跑。](https://hackaday.com/2017/04/01/ask-hackaday-which-balaclava-is-best-for-hacking/)

这个黑客的硬件方面是基于 Attiny85 的 Digispark，其克隆版本可以低至 1.50 美元，这取决于你愿意等待多久从中国发货。即使是官方的也只有 8 美元，尽管在我写这篇文章的时候还没有。将这东西封装在黑色收缩管中可以防止它短路，作为一个额外的奖励，让它看起来像合法的黑客。当然，如果你能买一个这样的小家伙，并在上面安装橡胶鸭子固件，那也不算什么。

为了使它更容易使用，官方的橡皮鸭运行用类似 BASIC 的脚本语言编写的脚本。[托马斯·C]使用了一个由[马库斯·门斯] 开发的名为 [duck2spark 的工具，它可以让你获得一个橡胶 Ducky 脚本(已经由 Hak5 作为开源发布)并将其编译成二进制文件，以便闪存到 Digispark。](https://github.com/mame82/duck2spark)

没有把剧本复制到原版 Ducky 的 microSD 卡上那么方便，但是你想要不到原版 1/10 的价格？就像我们在[之前的受 Hak5 产品](https://hackaday.com/2018/05/15/diy-pi-zero-pentesting-tool-keeps-it-cheap/)启发的 DIY 构建中所看到的那样，代价通常是易用性的代价。

【感谢 Javier 的提示。]