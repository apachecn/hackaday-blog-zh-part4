# 令人兴奋的图片来自 ATtiny85

> 原文：<https://hackaday.com/2022/04/12/mindblowing-graphics-from-an-attiny85/>

[rg pf lug]写了他的[非常好的图形库](https://github.com/GoergPflug/AttinyStreamGfxApi)。它有多层，两个文本控制台，灰度，内部半色调和精灵。它可以实现许多经典的图形技巧和演示。哦，对了，我们有没有提到它是在一个奇怪的*剧院和一个 I2C·有机发光二极管的屏幕上播放的？！*

这是一件了不起的作品——如果你问我们这是否可能，我们可能会说“不”。现在，您可以在自己的项目中使用它了。GitHub repo 充满了演示，展示了从多层之间的切换，极快的文本滚动，动画，boing 球，甚至是 Wolfenstein 风格的光线投射器。在 85 号公路上。

下面有一个演示视频，展示了这一切，但老实说，你必须想想什么会被适当地惊叹。例如，第一个演示似乎只是在静态文本上有一个图形波。没什么大不了的？它将灰度层混合在一起，并实时抖动成黑白的有机发光二极管！在 85 号公路上。

虽然这个库是用 C++编写的，但如果你愿意，甚至有几个例子可以说明如何将它与 Arduino 的 Wire 库集成在一起。我们不知道你是怎么想的，但这让我们想快速组装一个 ATtiny85 和 SSD1306 有机发光二极管演示板，开始玩一玩。这不仅是一个惊人的技巧，而且也是一个有用的方法，可以为你正在进行的任何项目添加图形和一个漂亮的控制台。

我们有没有提到这都是在 85 年前完成的？在 I2C 上空？太棒了。

 [https://www.youtube.com/embed/WNJQXsJqSbM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WNJQXsJqSbM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

