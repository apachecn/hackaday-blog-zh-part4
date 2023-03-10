# 微型弹球机也运行 X86 代码

> 原文：<https://hackaday.com/2022/07/21/tiny-pinball-machine-also-runs-x86-code/>

随着拱廊变得越来越罕见，许多弹球爱好者正在将这些复杂的机器搬到地下室、车库和客房的家中收藏。但是如果你不够幸运，住在一个可以支持像弹球机这样占用空间的爱好的家里，有一些解决这个问题的方法。例如，这款手机可以放在你的手掌上,而且恰好可以运行一些与其尺寸相当的令人印象深刻的软件。

不过，这台机器不像它的大型同类那样是一台机械弹球机。它本质上是一个 3D 打印的外壳，看起来像一个连接着两个屏幕的弹球机。它确实有一个工作活塞用于发射球，侧面有两个按钮用于近似真实性，但它实际上运行的是 *Pinball Fantasies* —一个旨在从 90 年代开始在 x86 硬件上运行的 Pinball 模拟器。它的内部有一个 ESP32，它的计算能力刚刚够运行一个 x86 模拟器，可以在 DOS 下加载这些游戏。

该游戏包括触觉反馈，并以每秒 60 帧的速度向前推进，鉴于游戏的微小尺寸，这确实将弹球体验带到了最高水平。从物理和软件的角度来看，在一个小空间里安装很多东西都令人印象深刻。对于更多全尺寸的数字弹球构建，[看看这个，它非常接近于复制真实的东西](https://hackaday.com/2014/06/10/digital-pinball-with-force-feedback/)。

 [https://www.youtube.com/embed/0JSB5lK9SYs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0JSB5lK9SYs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

