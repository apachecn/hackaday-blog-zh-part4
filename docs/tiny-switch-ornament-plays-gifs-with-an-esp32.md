# 小开关饰品用 ESP32 播放 gif

> 原文：<https://hackaday.com/2021/12/19/tiny-switch-ornament-plays-gifs-with-an-esp32/>

这些天来，我们黑客所能制造的东西不断让我们感到惊讶，(除了电子产品短缺之外)我们可以获得令人难以置信的一系列部件，这些部件的规格在几年前还会让我们倾家荡产，在更久以前还只是幻想。很高兴看到人们只是为了好玩而建造一次性产品，尽管目前很难获得实际交付的零件。例如，[看看这个由【Scott bez 1】](https://www.youtube.com/watch?v=zJxyTgLjIB8)创造的微型任天堂 Switch，它可以在 1.14 英寸的液晶显示器上播放 SD 卡中的动画 gif。

显然，这样一个小的黑客需要一个定制的 PCB，这是 KiCAD 的工作。配备了 LCD 的 3D 模型，使用 Fusion 360 绘制了外壳和 PCB 轮廓。PCB 上有一个 LilyGo ESP32 模块，用于所有繁重的工作，WiFi 增加了一些尚未探索的有趣的未来功能。该设计是尽可能的紧凑，而不会将 PCB 工艺的极限推得太远，包括一个将无源器件偷偷放入 SD 卡体内的巧妙技巧！这是我们将考虑的另一个节省空间的想法。

[![](img/5dc2ea6cb9c5fe19c2a649b81f88cd5d.png)](https://hackaday.com/wp-content/uploads/2021/12/miniswitch_detail.jpg)

总而言之，这是一个整洁的小程序，展示了一些好的建模和构建技术，以及一个好看的最终结果。您可以在 GitHub 的[项目中找到参考代码，但截至发稿时，硬件设计尚不可用。](https://github.com/scottbez1/SwitchOrnamentReference)

虽然这个项目缩小了开关，但这里有一个反其道而行之[并加大了它的尺寸](https://hackaday.com/2021/04/05/giant-nintendo-switch-is-actually-playable/)，如果你有一个开关精简版，但渴望一点现代充电魔法，那么不要再看这个 [Qi 无线充电黑客了。](https://hackaday.com/2021/10/13/adding-wireless-charging-to-the-switch-lite/)

 [https://www.youtube.com/embed/zJxyTgLjIB8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zJxyTgLjIB8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[JP]的提示！