# 适用于您电脑桌面的迷你 USB 显示器

> 原文：<https://hackaday.com/2021/06/20/a-mini-usb-display-for-your-pc-desktop/>

到目前为止，大多数黑客读者可能会习惯于 USB 显示适配器，它们最常见的形式是通过无处不在的串行接口传输 DisplayPort。用笔记本电脑连接投影仪和其他屏幕变得轻而易举，人们在做演示时“我的笔记本电脑能在会场工作吗”的压力已经一去不复返了。[Avra Mitra]的 STM32 微型显示器可能不会提升到这些令人眼花缭乱的高度，但它至少兑现了通过 USB 端口连接的小型彩色液晶显示器再现桌面的承诺。

虽然不是通过任何 DisplayPort 魔法，而是依赖于一个 Python 脚本，该脚本可以连续抓取屏幕并通过 USB 传输到微控制器，微控制器在 tun 中将其显示在显示器上。正如你在下面的视频中看到的，它声称可以达到每秒 6 到 7 帧，同时承认还有很大的改进空间。

尽管目前它的实用性有限，但我们可以看到，经过一些改进后，这个想法可能会在一个非常基本的显示器上使用。与此同时，更传统的显示器采取既定路线[将专用控制器板与 LCD 面板](https://hackaday.com/2021/02/25/diy-usb-c-touch-monitor-is-all-polished-brass/)配对。

 [https://www.youtube.com/embed/oFxuoMdBxJk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oFxuoMdBxJk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示。