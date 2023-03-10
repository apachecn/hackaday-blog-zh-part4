# 厄运？在你的简历里？比你想象的更有可能！

> 原文：<https://hackaday.com/2022/06/12/doom-in-your-bios-more-likely-than-you-think/>

我们已经看到黑客在各种各样的设备上运行 *DOOM* ，从台式电话到怀孕测试。现在，最后的边界已经被征服——我们让 *DOOM* 在 x86 机器上运行。当然，为了确保我们充分利用您的电脑硬件，我们必须放弃操作系统。这里有两种方法可以让你在后台运行经典的 shooter，而不会有大量臃肿代码的负担。

[【NIC 3-14159】实现了第一个](https://github.com/nic3-14159/coreDOOM)版本作为 coreboot 的有效负载，coreboot 是 x86 机器的开源 BIOS/UEFI 替代品。有些人可能会说它不完美——它没有声音支持，只能与 PS/2 键盘一起工作，退出游戏会让你的电脑死机。然而，它是可玩的，它适合你的 BIOS 闪存芯片。

但是如果你的电脑还没有免费的 BIOS 替换呢？你可能会喜欢这个 UEFI 模块 *末日*端口，最初由[Warfish]制造，然后由[Cacodemon345]构建。要运行这个程序，你只需要编译二进制文件和一个 UEFI shell，然后使用 UEFI 菜单中的“加载 EFI shell”选项——这是现在经常遇到的。这个版本也没有声音，但由于 UEFI 为其有效载荷提供的所有设施，它的功能更加全面。

当然，有更有效的方法来杀死你电脑上的恶魔，但即使从游戏的角度来看它们不一定实用，这两个项目也是 Coreboot 和 UEFI 有效载荷的不错的例子。像 coreboot 这样的 BIOS 替代品占用的空间如此之小，我们甚至看到 Windows 3.1 与 coreboot 一起放在 BIOS 芯片中。甚至想知道 UEFI 是什么？[这是给你的入门书。](https://hackaday.com/2021/11/30/whats-the-deal-with-uefi/)而且，如果你不介意精简版 Linux 安装的异常膨胀，这里有一个完全为运行 *DOOM* 而构建的 Linux 映像[。](https://hackaday.com/2022/06/09/a-linux-distribution-for-doom/)

 [https://www.youtube.com/embed/SZzlNfpt6Rs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SZzlNfpt6Rs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们感谢[WiFiCable]与我们分享这些！