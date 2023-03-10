# Cyberdeck 运行在苹果芯片上，尽管是 A12 而不是 M1

> 原文：<https://hackaday.com/2021/03/10/cyberdeck-running-on-apple-silicon-though-an-a12-not-m1/>

[Alta 的项目]建造了一个二合一的电脑平台,它不仅包含必要的 Raspberry Pi(在这种情况下是零),还避免了哑液晶显示器，并使用 iPad mini 5 作为显示器。

我们需要马上解决捐赠者的问题。有些人可能会认为这是异端邪说，虽然我们喜欢看到复古设备被亲切地修复，但循环利用温暖了我们的心，T2 也让大规模生产的塑料远离了垃圾填埋场。1991 年的 AST 386SX/20 笔记本电脑在一次网上拍卖中以 45 美元的价格售出，很可能永远不会被送往电脑博物馆。

为什么 Cupertino 的 iOS 会在网络平台附近？如果触摸屏比液晶面板好，那么后面有完整 OS 的平板电脑一定更好。你甚至可能会认为这是平板电脑外壳的自然发展，首先是键盘，然后是触控板。我们不知道如果不越狱，这两者都是可能的，但[Alta 的项目]只是使用了一个 lighting-to-USB dongle 和一个迷你 USB hub 来连接定制的分离键盘和 iPad，并在苹果 Magic Trackpad 上挥霍了一笔，用于无缝和无线多点触摸输入。

![Alta's Projects Cyberdeck Internal USB Wiring](img/0fda650d7b6c9d53b6bd57df41a74882.png)

Internal USB Wiring, Charging Circuit, and Pi Zero

视频构建(休息后)是轻的细节，但一个快速有趣的观看，在描述中有一个零件清单。它有一种迷人的休闲感，反映了[Altair 的项目]在建造中令人耳目一新的即兴方法。我们感谢[Tinfoil _ haberharery]对这个网络平台的认可，我们也立即想到了他的分离键盘和偏移显示器。提到一个想象中的“反乌托邦未来”,为一些 Dremel 切割和环氧树脂装配的粗糙表面开脱。也就是说，无论天启与否，安装在线性滑轨两端的磁铁肯定是一个不错的触摸。

![[Alta's Projects] Cyberdeck Linear Slide](img/fb0689555a0180636203fcb484f29572.png)

直线滑轨的磁性终点挡板

这可能是一个完整的项目，但【Alta 的项目】增加了一个可以访问 I/O 端口的 Pi，供未来的硬件黑客使用。VNC 提供了一种简单的方法，让 iPad 在通电时与 Pi 共享键盘、触控板和显示屏。Pi 还提供了一个辅助 eInk 显示器，即使在系统断电时也能显示系统信息或图形。另一个显示屏是 7 段式电池充电指示器，从 100%开始倒计时，在无线工作时非常有用，因为 Pi 和 iPad 都无法报告 9 个 18650 电池的状态。

我们喜欢这个 cyberdeck 可以很容易地升级到新的平板电脑上，并且考虑到 iPad 与快速释放磁性支架相连，它可以很容易地被移除以用于其他用途。说到升级换代，当这款 iPad 寿终正寝时，我们完全期待[显示屏也能获得新生](https://hackaday.com/2014/06/07/customized-ipad-lcd-screen-clips-onto-macbook-as-a-slick-second-screen/)。

 [https://www.youtube.com/embed/k_ONEso-ERg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/k_ONEso-ERg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

