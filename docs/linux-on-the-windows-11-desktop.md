# Windows 11 桌面上的 Linux

> 原文：<https://hackaday.com/2021/11/10/linux-on-the-windows-11-desktop/>

一个月前微软正式发布了 Windows 11。它的一个特点是能够像普通的 Windows 桌面应用程序一样并行运行 Linux GUI 应用程序。 *Ars Technica* 的[【吉姆·索尔特】仔细看了一下](https://arstechnica.com/gadgets/2021/10/the-best-part-of-windows-11-is-a-revamped-windows-subsystem-for-linux/)，宣称它像广告上说的那样有效。

这是 Linux 的 Windows 子系统(WSL)的发展，它已经存在了几年，但只是命令行形式。Linux 就是 Linux，当然有可能在屏幕上显示视觉效果，但是这样做需要通过一些限制。现在“WSLg”给人一种更流畅、更易上手的体验。

虽然对那些需要它的人来说非常有价值，但 WSLg 无可否认是一个小众特性。对于不同的需求，情况会有所不同。围绕这些部分，一个例子是让我们使用专有的 Windows 软件(如低级硬件驱动程序或特定于硬件的开发工具)，同时仍然为我们的工作流的其余部分保留 Linux 工具。

窥视一下幕后的情况也是很有趣的，因为它对两个操作系统之间的联系有启发性。一篇微软博客文章[描述了总体架构](https://devblogs.microsoft.com/commandline/wslg-architecture/)，我们很高兴看到开源工作得到了利用。通过将这项工作建立在 Wayland 的基础上，它比只与 X11 合作更具前瞻性。

坏消息是 WSLg 仅限于 Windows 11，至少目前是这样。Windows 10 上的 WSL 用户将不得不继续跳来跳去(我们[描述了一种使用 X11](https://hackaday.com/2021/08/05/linux-fu-the-windows-x11-connection/) 的方法)。)不幸的是，打开这扇门的同时也打开了[安全问题](https://hackaday.com/2021/09/24/this-week-in-security-somebodys-watching-microsoft-linux-ddos/)的大门，所以 WSL 还有很多工作要做。