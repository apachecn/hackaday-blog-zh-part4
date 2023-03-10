# 辅助功能应用程序从蓝牙按钮获得帮助

> 原文：<https://hackaday.com/2019/11/10/accessibility-apps-get-help-from-bluetooth-buttons/>

听说过微软的 Soundscape 吗？我们也没有。但显然，它和类似的应用程序，如 Blindsquare，为有视力问题的人提供了他们周围的环境。该应用程序在用户移动设备的后台运行，并对媒体控制做出响应，但如果你拄着拐杖四处导航，在手机甚至耳机上访问媒体控制可能不是很方便。[【jazz ang】着手制作可以控制应用程序的按钮](https://www.instructables.com/id/Arduino-Accessibility-Around-Me-Buttons-Switch-Con/)像这样的按钮可以与拐杖集成在一起，或者位于一个方便的位置。

有四个感兴趣的按钮。播放/暂停、下一页、上一页和主页。还有一个静音按钮和一个附加按钮，您可以在手机的辅助功能设置中使用。每个按钮对于 Soundscape 都有特殊的功能。比如接下来会描述你眼前的兴趣点。Soundscape 在 iPhone 上运行，因此蓝牙是创建按钮的显而易见的选择。

为了简化事情，该项目使用了 Adafruit Feather nRF52 Bluefruit 板。鉴于它与 Arduino 兼容，并提供开箱即用的蓝牙人机接口设备(HID)，除了连接开关和一些上拉电阻，几乎没有其他硬件工作要做。这将使电路很容易贴在几乎任何地方。

软件方面，事情也不太难。这个库提供了所有你需要的蓝牙 HID 设备，一旦设置好了，发送按键到手机就非常简单了。这是一个很好的例子，说明了由于处理所有细节的抽象的可用性，如此多的任务变得多么简单。由于 Bluetooth HID 设备只是一个键盘，您可能会想到这种设置的许多其他用途，只需对软件进行一些小的更改。

当蓝果第一次出现时，我们把它盖了回去。我们不知道如何将它安装在手杖上，但我们记得类似的东西[附在剑](https://hackaday.com/2018/08/16/welcome-to-the-internet-of-swords/)上。

 [https://www.youtube.com/embed/YEX6B0baSmM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YEX6B0baSmM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/5aFlNRv771k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5aFlNRv771k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

