# 互联网连接的电子纸留言板

> 原文：<https://hackaday.com/2020/09/25/internet-connected-e-paper-message-board/>

你还像 80 年代一样在纸上写笔记然后贴在冰箱上吗？好吧，如果你是，你读了这个网站，你可能想升级到一些更 21 世纪的东西。而且，多亏了机器人制造商[詹姆斯·布鲁顿]，你可以把你上个世纪的老式留言留在身后，因为他有一个教程向你展示如何建立一个互联网连接的电子纸信息显示板。此外，如果你有一个树莓派，一个电子纸显示器和适配器只是躺在那里无所事事，那么这个项目的成本将低于纸张和磁铁的成本。

撇开讽刺不谈，这是一个相当不错的项目。如前所述，它的基础是一个覆盆子 Pi ——[ James]使用 Pi 4，但是你也可以使用一个旧的、低功耗的模型。这为他在网上找到的便宜的电子纸显示器提供了动力，它带有必要的 Pi 适配器，以及一个 python 库来写入显示器。[James]使用一个 Google Sheet 作为留言板的云存储，有一些 python 代码来访问 Sheet 中的单元格，如果有任何变化，就将它们打印在显示器上。cron 作业每 5 分钟运行一次脚本，以捕捉消息中的变化。

和[James]做的大多数项目一样，他在视频中给出了一个很好的概述，并回顾了寻找硬件、编写和更新脚本的过程。他把他为这个项目创作的剧本和细节以及 CAD 文件放到了 GitHub 上。[James]之前已经在网站上出现过几次，看看[的一些](https://hackaday.com/2020/02/26/sonic-the-self-balancing-robot-face-plants-and-the-challenges-of-sensor-integration/)他的[项目](https://hackaday.com/2018/06/11/james-bruton-is-making-a-dog-opendog-project/)。

 [https://www.youtube.com/embed/cGsRJhoF5yY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cGsRJhoF5yY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

