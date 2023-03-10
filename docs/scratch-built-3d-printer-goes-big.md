# 白手起家的 3D 打印机变大了

> 原文：<https://hackaday.com/2020/11/04/scratch-built-3d-printer-goes-big/>

不久前，购买一台可靠的 3D 打印机曾经是一件相当昂贵的事情。许多人选择建造自己的打印机，几年来，我们被令人印象深刻的定制设计所淹没。但正如你所料，随着体面的 3D 打印机价格跌至谷底，定制版本已经基本枯竭。

可以说，在 2020 年，你愿意建造而不是购买的唯一原因是你想要非常具体的东西。这正是[【乔森迪】最终建造*大 F…打印机*或 BFP](https://www.joshendyblog.net/big-3d-printer-bfp/) 的原因。毫无疑问，F 代表有趣或友好。不管怎样，这肯定是件特别的事。凭借 300 毫米的体积和重型 Z 轴，这种全封闭的 CoreXY 机器可以随时处理他扔给它的任何东西。

[![](img/18c16adb6abcce6f31bb0d88c7532f69.png)](https://hackaday.com/wp-content/uploads/2020/10/bfp_detail.jpg) 尽管如此,【乔森迪】还是尝试了几次才如愿以偿。事实上，这台机器的原型甚至不是 CoreXY，它最初是一个 H-Bot。在他的文章中，他回顾了自由党所做的不符合他期望的事情，以及他用什么来代替它们。因此，当摇摇欲坠的丝杠和仿制的 V6 发动机都有所欠缺时，它们最终分别被滚珠丝杠和正宗的 E3D 赫莫拉所取代。

为了控制这个庞然大物，[Joshendy]在运行 Klipper 的树莓 Pi 和 BigTreeTech SKR Pro 上使用 OctoPrint。OctoPrint 使他能够远程控制和监控打印机，并在外壳内安装一个摄像头来监视事物，而 SKR 板上的 Klipper 固件将 3D 打印的所有计算昂贵的方面推到 Pi 中功能更强大的 ARM 芯片上。最终结果是通过 TMC2130 驱动器对步进器的控制[比其他方式更快、更精确。](https://hackaday.com/2017/12/26/fast-3d-printing-with-raspberry-pi-but-not-how-you-think/)

如果你不介意修补，一台便宜的入门级桌面 3D 打印机对大多数黑客和制造商来说已经足够好了。如果你需要更强大或更可靠的产品，总有像 Prusa 和 Ultimaker 这样的[高端产品可供选择。很少有人*需要*来建造像 BFP 这样严肃的东西，但是当他们需要的时候，我们很高兴他们把他们送给我们。](https://hackaday.com/2018/10/22/a-close-look-at-the-prusa-i3-mk3/)

 [https://www.youtube.com/embed/8EfwWAECTHE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8EfwWAECTHE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

