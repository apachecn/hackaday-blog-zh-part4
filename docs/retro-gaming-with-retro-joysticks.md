# 使用复古操纵杆的复古游戏

> 原文：<https://hackaday.com/2022/01/30/retro-gaming-with-retro-joysticks/>

在原始硬件上玩旧视频游戏的最大原因之一是模拟器和现代控制器无法复制这些游戏最初的体验。这对于旧的 PC 游戏也是如此，所以如果你想使用你原来的 Sidewinder 方向盘或古董罗技操纵杆，你需要像[Necroware]的[游戏端口适配器这样的东西来让它们与现代硬件](https://github.com/necroware/gameport-adapter)进行通信。

在 USB 成为标准之前，将控制器连接到 PC 的方式是通过游戏端口，通常在声卡上找到。这在现代控制器中已经消失很久了，所以构建的 USB 接口依赖 Arduino 来完成翻译。具体来说，该适配器被设计为几种不同模拟操纵杆的通用适配器，并且适配器上的一系列 DIP 开关选择适当的模式。休息后看看视频。该适配器还能够自动校准操纵杆，这是必要的，因为控制器中的无源组件现在的行为方式往往不同于它们新出现时的行为方式。

我们很多人都有这个时代的操纵杆和方向盘，所以如果你想体验飞行模拟器 5.0，就像 1993 年一样，只需要一台 Arduino。此外，如果你想在裸机上运行这些程序，而不是在模拟器上，实际上有可能[构建一台新的英特尔 486 游戏 PC](https://hackaday.com/2021/04/17/dos-gaming-pc-gets-necessary-updates/) ，它的运行方式几乎与 90 年代的 PC 完全一样。

 [https://www.youtube.com/embed/947DewHwbsE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/947DewHwbsE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/tSJLgCD8jeM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tSJLgCD8jeM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

