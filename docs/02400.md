# 如何连接世嘉控制器，并使其无线化

> 原文：<https://hackaday.com/2019/03/18/how-to-interface-sega-controllers-and-make-them-wireless/>

世嘉 Genesis，或在北美以外被称为 Mega Drive，是一款受欢迎的游戏机，因为世嘉做了任天堂没有做的事情。抛开不合时宜的营销笑话不谈，它将快速滚动的 16 位游戏带到了家用游戏机平台，多年来赢得了许多粉丝。你可能会发现自己想要与旧的控制器硬件进行交互，在这种情况下，[【Jon you sel】可以提供帮助。](https://jonthysell.com/2014/07/26/reading-sega-genesis-controllers-with-arduino/)

[Jon]已经完成了理解 Sega 控制器接口所需的工作，并在 Github 上分享了他的工作。这个界面很有趣，并且根据所使用的控制台和控制器硬件的不同而不同。最初的主系统有 D-pad 和两个按钮，控制器上的六个开关仅使用六个引脚。在状态机式的 6 按钮键盘设置变得更加复杂之前，3 按钮 Genesis pad 变得更加高级。

[Jon]有益地分解了各种接口，并使它们与 Arduinos 的接口变得相对容易。分享这样的工作可以让其他人站在巨人的肩膀上，建立自己的项目。这为我们带来了工作，比如[【丹尼洛】的无线创世纪控制器制造](https://hackaday.io/project/164275-a-diy-bluetooth-sega-genesismega-drive-joystick)。通过将 Sega 协议的知识与一些现成的 Arduinos 和蓝牙部件相结合，它使得快速制作无线控制器变得容易。

在当今时代，大多数控制台控制器可以通过各种简单的解决方案(通常是 USB)与 PC 轻松连接。不过，你可能想尝试一些更难的东西，比如将现代任天堂控制器连接到 C64。休息后的视频。

 [https://www.youtube.com/embed/CP_Y1NyTjrU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CP_Y1NyTjrU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

