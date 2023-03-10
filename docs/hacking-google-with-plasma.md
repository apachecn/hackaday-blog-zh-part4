# 用等离子黑谷歌

> 原文：<https://hackaday.com/2022/10/10/hacking-google-with-plasma/>

谷歌最近制作了一些视频来强调网络安全。下面的视频是第三集，它讲述了一个关于第一个碰撞测试假人的有趣故事。然而，真正有趣的部分是关于一个用来入侵电脑的 USB 等离子球的故事。建造地球仪的人之一在最近的一篇博文中讲述了地球仪内部的故事，这篇博文有更多的技术细节。

问题中的攻击发生在 2012 年，当时人们开始意识到将随机 USB 驱动器插入他们的计算机不是一个好主意。然而，一个可爱的小等离子球只是从端口获取电力，会有什么危害呢？

正如我们所知，这可能非常危险。问题中的地球仪是现成的，但在电缆的底部有一个 ATMega32U4 芯片。LUFA USB 库提供键盘设备仿真。这个想法是，地球将等待时机，然后输入一个危险的有效载荷。

键盘尤其阴险，因为操作系统通常只是静静地接受它们的存在。不会提示您允许使用键盘或安装驱动程序。除非，他们发现，你用的是 Mac。但不要对 Mac 的安全性印象太深。它显示对话框的唯一原因是它试图找出一个未知键盘的布局。

解决办法很简单。只要你在黑客攻击，你还不如撕掉一个苹果 USB ID，这样操作系统就知道它应该是什么样的键盘。问题解决了。你可以在视频中看到 8:30 左右的等离子球。

这是一个有趣的故事，我们已经不是第一次看到特洛伊木马接近 T1 来窃取机密了。当然，你可以做一个[真正破坏性的 USB 设备](https://hackaday.com/2017/02/19/the-usb-killer-now-faster-better-more-anonymous/)，但是我们不建议这样做。

 [https://www.youtube.com/embed/TusQWn2TQxQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TusQWn2TQxQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

