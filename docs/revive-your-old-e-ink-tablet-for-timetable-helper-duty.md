# 恢复你的老 E-Ink 平板电脑的时间表助手的职责

> 原文：<https://hackaday.com/2022/08/02/revive-your-old-e-ink-tablet-for-timetable-helper-duty/>

在我们的抽屉里，会有一些我们已经忘记的旧设备，也许我们应该让它们为我们服务。[Jonatron]在他的抽屉里找到了一个 Nook Simple Touch 凭借其电子墨水屏幕、无线连接和可用的 Android 版本，这款 2011 年的电子阅读器有勇气永远显示职责。可悲的是，背面的软触摸覆盖物分解成一团粘糊糊的东西，正如 soft touch 所做的那样，锂离子电池已经耗尽，软件支持也乏善可陈。很多平板电脑都可能出现这两种情况，这就是为什么我们很高兴[Jonatron]分享了他关于这款电子阅读器复兴的故事。

背面的柔软触感层并没有因为酒精而消失，但幸运的是，附近有一个丙酮瓶，丙酮擦洗有助于消除令人不快的粘性。这款平板电脑的充电电路并不复杂——平板电脑无法通过 MicroUSB 输入启动，而且[乔纳森]将 5 伏电压从 USB 电缆直接接入电池输入端。请注意，这可能是不建议的，因为锂离子电池的范围是 3 伏到 4.2 伏，需要一个调节器，但[Jonatron]说它一直工作得很好。

通常，你可以在你的本地网络上安装一个网络服务器，为一个页面提供有用的信息，添加代码定期刷新页面——但 Nook 的浏览器不支持自动刷新。为了不被阻止，[Jonatron]为 Nook 的 Android 安装写了一个应用程序；生根是必需的，但进行得天衣无缝。Android 安装是旧的，Android Studio 已经不能下载了，所以他使用了一个旧的开发工具包，不知何故仍然可以在网上找到。仍然有一个由 Python 编写的小型 web 服务器运行在备用 Pi 上，为应用程序获取数据提供条件。遵循最佳黑客传统，应用程序和服务器[都是开源的！](https://github.com/jonatron/trook/)在 3D 打印支架的帮助下，这款平板电脑现在可以显示火车发车时间表——对于像这样的老式电子阅读器来说是完美的应用。

在抽屉里找到一个简单的角落？现在你知道你可以很容易地将其转换成一个黑客攻击的电子墨水显示器！我们以前见过无数的平板电脑修复，更换了[充电器 IC](https://hackaday.com/2020/11/24/trashed-tablet-lives-again-thanks-to-new-charger-ic/)和 [eMMC 驱动器，](https://hackaday.com/2018/03/06/hot-air-surgery-revives-a-cheap-windows-tablet/)把它们变成了[视频电话](https://hackaday.com/2020/04/25/checking-in-on-relatives-using-old-android-tablets/)和[智能家居控制器，](https://hackaday.com/2021/09/15/smart-home-hack-breaks-down-walls-figuratively-and-literally/)甚至还有[修复数据库](https://hackaday.com/2021/12/14/what-really-goes-wrong-with-your-tablet/)来帮助你的复兴努力。在我们的上一期 Hackaday Prize 分期付款中，我们已经得到了相当多的类似项目， [Hack It Back，](https://hackaday.com/2022/06/13/2022-hackaday-prize-hack-it-back-and-make-it-yours/)我们希望在我们的通配符回合中看到更多这样的重建！