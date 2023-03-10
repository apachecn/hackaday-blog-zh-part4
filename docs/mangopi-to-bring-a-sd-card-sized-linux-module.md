# MangoPi 将带来一个 SD 卡大小的 Linux 模块

> 原文：<https://hackaday.com/2022/04/01/mangopi-to-bring-a-sd-card-sized-linux-module/>

今天的小型设备是来自[MangoPi]的一款名为 M-Core 的[小型模块化系统](https://twitter.com/mangopi_sbc/status/1507650871785816070) (Twitter 链接， [nitter 代理](https://nitter.net/mangopi_sbc/status/1507650871785816070))，具有四核 A53 CPU 和 1gb RAM。因此，它非常能够运行 Linux，甚至支持 HDMI 输出！仔细看看 devboard 的图片，我们可以发现三个 USB 2.0 端口的痕迹，似乎是两个用于 MicroSD 或 WiFi 卡的 SDIO 接口，以及一个带有终端网络的以太网 MagJack。这是一组不错的接口，可以与我们对 Pi Zero 的期望相媲美！

更重要的是，这个模块和 SD 卡本身一样小——或者像我们业余爱好者在项目中使用的有机发光二极管显示器一样小。在如此小的内存中拥有 Linux 的强大功能当然是值得一看的！该模块的背面大部分是平的，除了 CPU 另一侧的几个去耦电容器——看起来是一个全能的 H616。在它的顶部，我们可以看到 CPU 本身，一个小型降压调节器和一个 DDR3 RAM 芯片，以及紧密包装的无源器件。DFN8 QSPI 闪存芯片甚至还有一个未被占用的空间——有了足够轻量的操作系统版本，您也许可以将您的 MicroSD 卡专用于存储。

[![](img/4f0d6221db762c8a67ab9576c85da331.png)](https://hackaday.com/wp-content/uploads/2022/03/mangopi_detail.jpg) 的开发板使用类似“FlexyPins”的连接技术[我们最近已经报道过](https://hackaday.com/2022/03/07/flexypins-might-help-with-those-pesky-castellated-modules/)，【MangoPi】说[他们在淘宝上买了那些引脚](https://twitter.com/mangopi_sbc/status/1508631148435750912)。想到让 HDMI 通过这样的连接，我们不禁有点觉得好笑，但它似乎足够好了！像这样的城堡式模块相对容易使用，因此从 devboard 中取出该模块并将其放到 PCB 上应该不难。据报道，下一步是将 Armbian 移植到该板上，这可能会解决相当多的软件支持障碍。

在过去的几周里，MangoPi 一直在他们的 Twitter 页面上发布更新，而且，随着格式的出现，许多问题都没有得到解答。为什么 devboard 只显示一个线性调节器，而我们通常期望它最多提供 1 A 电流？我们会得到内存更高的版本吗？价格会是什么样子？这个模块会上市吗？我们只能希望，但如果确实如此，我们肯定会看到一些项目采用这些技术，无论是[智能眼镜](https://hackaday.com/2021/08/14/3d-printed-smart-glasses-put-linux-in-your-face/)、[智能显示器](https://hackaday.com/2019/07/31/open-source-smart-display-takes-the-long-way-around/)、[手机](https://hackaday.com/2017/09/12/hackaday-prize-entry-retrofit-a-nokia/)、[手持设备](https://hackaday.com/2022/02/04/the-fifteen-dollar-linux-computer/)还是[恶意壁式充电器](https://hackaday.com/2021/07/26/wifiwart-boots-linux-moves-to-next-design-phase/)。像往常一样，社区创造或破坏一个 SBC，我们将密切关注这一个。

我们感谢[WifiCable]和[DjBiohazard]与我们分享这些！