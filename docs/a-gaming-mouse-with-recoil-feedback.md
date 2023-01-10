# 一种具有反冲反馈的游戏鼠标

> 原文：<https://hackaday.com/2020/09/08/a-gaming-mouse-with-recoil-feedback/>

早在 20 世纪 90 年代中期，隆隆声首次成为游戏主流，从那以后，它已经成为使用游戏手柄的游戏机玩家的必备之物。它在 PC 上不太流行，因为大多数玩家依赖于无噪音的键盘和鼠标。然而，创新是可能的，[和【ilge】为射手们组装了一个改良的鼠标，它有一个极好的后坐力反馈装置。](https://www.instructables.com/id/DIY-Backfire-Mouse-in-the-Game-PUBG-Gameplay/)

反馈效果由 Arduino 运行，Arduino 从主机上运行的 Python 程序接收串行数据。当鼠标被点击时，Python 程序通知 Arduino，然后 Arduino 反复来回触发一组四个螺线管来产生反馈效果。螺线管由继电器触发，这是切换这种负载的一种简单方式，尽管我们怀疑它可能不会随着时间的推移而保持良好，因为快速点火率和随着时间的推移由螺线管的高涌入电流引起的火花损坏的可能性。

这是一个简单的构建，但却给原本不起眼的电脑鼠标增加了一个很好的触觉反馈效果。虽然我们不希望很快看到专业人士使用这款设备，但这是一个很好的概念，可以增加射手的体验。类似的硬件也可能在虚拟现实环境中发挥巨大作用。触觉技术的艺术状态继续快速发展，我们迫不及待地想知道接下来会发生什么。休息后的视频。

 [https://www.youtube.com/embed/Jw-RmpuH7JU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Jw-RmpuH7JU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

