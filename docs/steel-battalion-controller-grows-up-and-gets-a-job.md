# 钢铁营指挥官长大并找到一份工作

> 原文：<https://hackaday.com/2019/09/13/steel-battalion-controller-grows-up-and-gets-a-job/>

我们要大胆地说，最初 Xbox 上的钢铁军团控制器是有史以来最令人印象深刻的视频游戏外设。旨在让玩家感觉他们真的在“垂直坦克”的驾驶舱中，控制器具有双控制杆，三个踏板，一个档位选择器，以及几十个按钮，开关和旋钮。不幸的是，除了玩*钢营*和它的续作，你对这个巨大的控制台没什么可做的。

[![](img/0bd7d07eed2c11dc6892dfad99327149.png)](https://hackaday.com/wp-content/uploads/2019/09/sbcon_detail.png)

HID Report Descriptor

但现在，在游戏发布近 20 年后， [[Oscar Sebio Cajaraville]不仅开发了一个开源驱动程序](https://medium.com/@oscarsc/writing-a-driver-for-the-steel-battalion-controller-e1e4311f1a40)，让你可以在现代 Windows 机器上使用臭名昭著的机甲控制器，而且他还是开发新游戏团队的一员，实际上可以用它来玩游戏。虽然想象在光荣的 4K 驾驶未来战斗机器人的游戏玩家可能会有些失望地发现，这一次，*钢* *营*控制器被用来操作一件建筑设备。

在他的博客文章中，[Oscar]重点讲述了为一个几十年前的控制器开发一个现代 Windows 驱动程序的过程。它有助于最初的 Xbox 使用本质上只是 USB 1.0 控制器的重新布线，所以连接它不需要任何特殊的硬件。不幸的是，虽然控制器使用 USB 与控制台通信，但它与 USB-HID 不兼容。

事实证明，微软实际上提供了一个开源的示例驱动程序，它是专门设计来将非 HID USB 设备适配到系统可以识别的合适的游戏控制器中的。这给了[奥斯卡]一个完美的起点，但他仍然需要探索控制器的端点，并解码它通过线路发送的数据。这包括为控制器创建一个 HID 报告描述符，如果你曾经与一个古怪的 USB 设备交谈，这是一个巧妙的技巧。

最终，[Oscar]创造了一个驱动程序，允许玩家在他的游戏 BH Trials 中[使用*钢铁营*控制器。不幸的是，有一个问题，在 Windows 10 安装驱动程序之前，需要由可信的认证机构对其进行签名。由于他不能完全证明这一步的花费，他写了第二个帖子](https://store.steampowered.com/app/1067080/BH_Trials/)[详细说明了关闭驱动程序签名的要求，这样你就可以让设备工作](https://medium.com/@oscarsc/how-to-use-the-steel-battalion-controller-on-windows-10-2e21aa8ccd28)。

今年早些时候，我们看到了围绕*钢铁营*控制器建造的[令人难以置信的模拟器，外部“教练”可以观看你的比赛，并给你在虚拟战场上生存的提示。但即使是那个项目还是用了原来的游戏；希望一个开源驱动程序能让这种外设在微软最新的操作系统上工作，这将有助于刺激更令人印象深刻的黑客技术的发展。](https://hackaday.com/2019/03/02/an-epic-mech-cockpit-build-for-steel-battalion/)

 [https://www.youtube.com/embed/IkoGfoX_oEE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IkoGfoX_oEE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

