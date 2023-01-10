# Sierpinski PCB 圣诞树

> 原文：<https://hackaday.com/2020/12/04/sierpinski-pcb-christmas-tree/>

又到假期了！这意味着是时候拿出烙铁和 RGB LEDs 灯了！如果你要制作一个定制的 PCB 来安装这些 led，你会注意到你的订单中只有几个 PCB 的副本，所以，不妨这样设计，就像[Landon Carter]所做的那样，你可以将它们组合成一个单独的 [Sierpinski 圣诞树](https://www.lycarter.com/2020-11-29/xmas-decorations)。

每个 PCB“树”都有三个连接，通过在 PCB 上焊接两个桥接之一，可以用作输入或输出。电源和信号在树中上下传递，而不是交叉传递，因此树的顶部有一个连接，底部有两个连接。这样，三角形中的每棵树都可以很容易地连接起来，并且每个三角形都可以很容易地连接到另一个三角形。每棵树都有三个 WS2812b-mini 可寻址 RGB LEDs，由外部 Arduino 控制。

第一笔 10 块 PCB 的订单到了，这就形成了 9 个成员的树，接下来是 27 个成员的树。在那之后，你需要一些非常高的拱形天花板来把它们挂在墙上。不过，从好的方面来说，一旦假期结束，所有东西都可以很容易地拆开，和其他装饰品一起打包。如果你也对 RGB LED 装饰品感兴趣，在[网站](https://hackaday.com/2016/10/30/just-in-time-for-christmas-a-diy-desktop-led-tree/)上有一些[和](https://hackaday.com/2017/01/01/wifi-controlled-christmas-ornaments/)供你细读。