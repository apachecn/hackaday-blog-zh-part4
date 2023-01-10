# 硬件中的 Pong 实际上

> 原文：<https://hackaday.com/2022/04/06/pong-in-hardware-virtually/>

我们是法尔斯塔德赛道模拟器的忠实粉丝。当然，它并不完美，但当你想快速完成一个简单的电路时，没有什么比它更好的了。但是当我们在法尔斯塔德看到 [*Pong* 或多或少完整的硬件实现时，我们被震撼了。不开玩笑。从](https://www.falstad.com/pong/)[的原始原理图](https://www.arcade-museum.com/manuals-videogames/P/PongSchematic.pdf)开始，有多个页面显示每个子电路，甚至是一个可玩的子集，你可以在你的浏览器中玩游戏。

但是等等…你可能注意到模拟器的组件菜单中没有 CRT 显示。这倒是真的，没有。但是，您可以编写 JavaScript 来与正在运行的模拟进行交互，因此显示是一段简单的 JavaScript 代码，它在预定的点对信号进行采样，并绘制相应的图形。甚至还有声音效果的音频输出，尽管这是模拟器内置的。

作为展示如何工作的示例，请看下面的代码片段:

```

// called every timestep, which is 6 nanoseconds of game time.
// we do as little work in here as possible.
function didStep(sim) {
   var c = clk.getVoltage();
   if (c == lastclk)
      return;
   if (c>2.5) {
// positive clock transition, increase x
   x++;
   if (x == 375) {
   x = -80;
   y++;
   if (sim.getNodeVoltage("VBLANK") > 2.5) {
// if we're in vertical blank, set y to 0
   y = 0;
   clearedY = -1;
   sim.setExtVoltage("PADTRIGGER1", 5);
   sim.setExtVoltage("PADTRIGGER2", 5);
}

```

只需在您最喜欢的浏览器中查看页面源代码，就可以看到全部内容。

如果你曾经想知道这样的东西是如何工作的，这不仅是非常有教育意义的，而且它也是一个很好的说明，你可以用 Falstad 模拟器和一些网页工作做什么。它给了我们很多想法。如果你对 Pong 电路本身感兴趣，我们真的很喜欢每一页如何分解电路的一部分，并解释它与相关的模拟。

别忘了你可以在法尔斯塔德尝试一下 [Arduino 程序。你甚至可以建造一台](https://hackaday.com/2021/06/11/circuit-vr-arduino-virtually-meets-analog/)[简单的模拟计算机](https://hackaday.com/2022/03/31/circuit-vr-the-wheatstone-bridge-analog-computer/)。