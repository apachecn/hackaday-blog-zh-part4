# 大屏幕上的 Arduboy

> 原文：<https://hackaday.com/2021/06/01/arduboy-on-the-big-screen/>

在 Hackaday，我们是 Arduboy 的忠实粉丝，但我们承认它的小屏幕并不完全适合长时间的游戏。有一些开源手持设备的 DIY 版本使用了更大的 SPI 有机发光二极管显示器，尽管在游戏开始停止之前，你对硬件可以做什么样的改变相对有限。但是正如[Nick Bild]用他的 Arduboy 家庭控制台展示的那样，入侵核心系统库开启了许多有趣的可能性。

为 Arduboy 编写的游戏利用一个公共库来处理所有底层硬件，其中包括一个`display()`函数，用于将图形数据推送到 SPI 连接的有机发光二极管显示器上。[Nick]所做的是重写该函数，以输出到运行在 TinyFPGA BX 上的自定义 VGA 生成器。他不得不删除对 Arduboy 的 RGB LEDs 的支持，因为他需要额外的引脚，但这应该不会在软件支持方面造成太大问题。

这确实意味着游戏需要根据修改后的库重新编译才能在他的硬件上运行，但由于 Arduboy 软件的绝大多数都是开源的，这不是什么大问题。我们特别喜欢超级游戏男孩风格的边框，你可以在显示器周围免费看到。

在这一点上，硬件看起来不像是一个控制台，而更像是一个装满跳线的试验板，所以我们有兴趣看到这个项目的逻辑结论。一个定制的 PCB，外壳，甚至可能支持使用原来的 NES 控制器将把这变成适当的系统值得任何黑客的游戏室。如果你想要的话，你甚至可以[把游戏放在定制的盒式磁带上](https://hackaday.com/2019/06/07/the-arduboy-community-rolled-their-own-cartridge/)，尽管一个[闪存芯片可以容纳系统的整个库](https://hackaday.com/2021/03/04/arduboy-fx-mod-chip-now-youre-playing-with-power/)会更方便一些。