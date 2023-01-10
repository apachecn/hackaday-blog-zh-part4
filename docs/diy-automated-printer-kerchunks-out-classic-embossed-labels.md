# DIY 自动打印机 Kerchunks 出经典压花标签

> 原文：<https://hackaday.com/2022/06/15/diy-automated-printer-kerchunks-out-classic-embossed-labels/>

对于我们的钱来说，几乎任何用途的最佳标签是那些压花的梁永能式不干胶标签，有凸起的白色字母的那种。它们就是有一些东西——凸起的字母只是乞求被触摸，它们的易读性是突出的，它们给项目带来了无与伦比的复古感，并且用那些手动 *kerchunkers* 之一创建一个字母的体验令人奇怪地满意。

但是，唉，那些手工标签制造商已经今非昔比了，正如安德烈·斯佩里迪奥(Andrei Speridiã)在他的手里分崩离析时所发现的那样。他没有抱怨，而是自动化了他的标签制作机，并把它变成了电脑外设。被称为“电子 TKT”的 DIY 标签打印机从他废弃的贴标机上取下菊花轮压花模具，并将其置于计算机控制之下。一个步进电机推动磁带前进，另一个步进电机将轮子旋转到正确的位置，而不是原来的棘轮机构，伺服机构负责切边工作。该过程重复进行，直到标签完成并整齐地切下，准备粘贴。ESP32 运行该机制，并提供一个 web 应用程序来编写标签和控制打印机。还有一个有机发光二极管展示，当然，还有一个浮雕标签。下面是视频演示。

我们不在乎[巴特·辛普森]怎么想，压花标签很酷，这让它们更酷。正如[Andrei]指出的，这也是绕过[肮脏的 DRM 诡计](https://hackaday.com/2022/03/30/freedmo-gets-rid-of-dymo-label-printer-drm/)的一个巧妙方法，一些公司正把它强加给标签制作公众。仅此一点就有理由为这个项目欢呼——但我们也不会抱怨美丽的摄影和出色的文档。

 [https://www.youtube.com/embed/F0E5adLQ-AY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/F0E5adLQ-AY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2022](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)