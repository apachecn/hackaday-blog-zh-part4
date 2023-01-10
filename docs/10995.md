# 虚拟赛车手在便携式 WS2812 赛道上一决高下

> 原文：<https://hackaday.com/2021/08/12/virtual-racers-battle-it-out-on-portable-ws2812-track/>

当然，现代视频游戏令人印象深刻，但你肯定不需要 4K 显示器或高速互联网连接来享受美好时光。一个完美的例子，看看[这个由【mirc emk】](https://hackaday.io/project/181115-diy-led-racing-game-open-led-race)拼凑的独特的一维赛车游戏。这个[Gerardo Barbarov Rostan]的开放式 LED Race 项目的变体已经按比例缩小，因此可以方便地运输，但至少现在，你仍然需要将它插入外部电源。

这个游戏非常简单。通过快速按下各自的按钮，玩家可以在由 60 个 WS2812 RGB LEDs 组成的线性“赛道”上驾驶他们的虚拟车辆比赛。用最基本的术语来说，他们按下按钮越快，代表他们的汽车的红色或绿色发光二极管移动越快。

[![](img/70e3c5a69ea5ae4bd2d89ca19d4cab10.png)](https://hackaday.com/wp-content/uploads/2021/08/1drace_detail.jpg) 但在实际操作中，赛车将会遇到的“山丘”增加了模拟重力，事情变得更有趣了。这些车也有一点惯性，即使你没有按下按钮，它们也会滑行。甚至还有可选的发动机声音，尽管与汽车的视觉表现一样，想要达到预期的效果需要一定程度的想象力。

这个游戏对硬件的要求很低，可以很容易地适应你的零件箱。除了 WS2812 LEDs 之外，您真正需要的是一个微控制器和两个按钮。这里[mircemk]使用的是 Arduino Nano，但是你可以使用几乎任何 MCU。为了使这个版本尽可能便携，按钮被内置在 PVC 板外壳中，但将它们放在一些有线遥控器中会使游戏更加舒适。

多年来，我们已经报道了几个项目，这些项目的目标是将不起眼的一串 RGB LEDs 变成一个互动的电子游戏。只要你有开放的心态，你就能[发现隐藏在闪烁的灯光中的整个世界](https://hackaday.com/2016/07/17/video-games-in-as-few-dimensions-as-possible/)。

 [https://www.youtube.com/embed/PkmuhKyfCGA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PkmuhKyfCGA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

