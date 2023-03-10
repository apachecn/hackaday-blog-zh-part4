# 看看任天堂是如何掌握双屏的

> 原文：<https://hackaday.com/2021/01/28/a-look-at-how-nintendo-mastered-dual-screens/>

当它首次宣布时，许多人对任天堂 DS 持怀疑态度。这款独特的双屏手持设备不是推动原始动力，而是旨在探索新的游戏风格。与 Game Boy Advance 甚至索尼的 PlayStation Portable 等更传统的手持设备相比，ds 似乎是日本游戏巨头的一场豪赌。

但它得到了回报。任天堂 DS 最终成为有史以来最成功的游戏平台之一，[正如【现代复古游戏玩家】在最近的视频](https://www.youtube.com/watch?v=kBgQJJ93nFM)中解释的那样，至少部分原因是其令人惊讶的图形能力。虽然它在技术上几乎在所有方面都不如 PSP，但任天堂几十年来挑战 2D 图形极限的经验使他们能够从硬件中挤出比许多人想象的更多的东西。

在某种程度上，任天堂 DS 可以被视为升级版 GBA。已经习惯了该系统的 2D 功能的开发人员在转换到 DS 时会有宾至如归的感觉。与以前的 2D 控制台一样，DS 有几种屏幕模式，支持移动、缩放、旋转和反射多达四个背景层的硬件加速。这使得实现伪 3D 效果变得容易且计算效率高，例如让多个背景图像以不同速度滚动来传达深度感。

[![](img/26047b2b1ddcab8251fb6b581829651f.png)](https://hackaday.com/wp-content/uploads/2021/01/dsgraphics_detail.jpg)

除了继承自 GBA 的 tile 和 sprite 2D 引擎，DS 还配备了一个基本的 GPU，负责处理 3D 几何图形和渲染。硬件加速 3D 一次只能在一个屏幕上使用，这意味着大多数游戏将在一个显示器上保留动作的特写视图，并使用第二个面板来显示 2D 图像，如空中地图。但是开发人员确实可以选择在每一帧的显示器之间切换，以降低的帧速率在两个面板上渲染 3D。该硬件还可以处理阴影，并包括对单元格阴影的集成支持，这在当时是一种特别流行的图形效果。

通过将任天堂 DS 的 2D 和 3D 硬件功能结合到一个屏幕上，开发者可以制作复杂的图形效果。[Modern Vintage Gamer]使用了*新超级马里奥兄弟*的例子，它在几层移动的 2D 位图上放置了一个详细的马里奥 3D 模型。最终，DS 的 3D 功能受到其 256 x 192 LCD 面板有限分辨率的限制；但考虑到 DS 问世时大多数人仍在使用翻盖手机，这在当时是令人印象深刻的。

与 Game Boy Advance 或[甚至是最初的“砖块”游戏男孩](https://hackaday.com/2020/08/05/the-game-boy-as-a-midi-synthesiser/)相比，黑客们似乎没有太多运气来开发任天堂 DS 的功能。但是，也许有了像这样更详细的回顾，社区将会受到启发，重新审视这个游戏历史上独一无二的条目。

 [https://www.youtube.com/embed/kBgQJJ93nFM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kBgQJJ93nFM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

