# 8 位 Atari 计算机支持 SVG 渲染

> 原文：<https://hackaday.com/2019/03/08/svg-rendering-comes-to-8-bit-atari-computers/>

将现代协议和技术引入老式计算机是黑客最喜欢的消遣，多年来，我们已经看到了一些绝对不可思议的硬件和软件项目，它们专门设计来做大多数人认为不可能的事情。当然，它们很少是实用的项目。但这从来都不是重点。

[![](img/9f07f19999837cc908287a1507cb4691.png)](https://hackaday.com/wp-content/uploads/2019/03/atarisvg_detail.jpg)

The product of 45 minutes of work.

今天，我们展示了另一个进入这一利基黑客途径的绝佳入口: [Renderific，一个由【Kevin Savetz】开发的在 8 位 Atari 计算机上渲染 SVG 的工具](https://github.com/savetz/Renderific)。麻省理工学院许可的程序是用 Turbo-BASIC XL 编写的，它允许 1200XL 和 800XL 这样的计算机不仅在屏幕上渲染图像，而且将其输出到附加的绘图仪。有些文件存在一些小问题，显然绘图仪出于某种原因将图像绘制颠倒了，但总的来说，我们现在可以将“SVG 渲染”添加到您可以用近 40 年的旧计算机做的事情列表中。

当然，那些熟悉这些 1980 年代的机器的人可能会想，他们有限的 CPU 怎么可能应付这样的任务。这就是不切实际的地方。根据[Kevin]的说法，根据图像的复杂程度，你可能要等很长时间。在他的测试中，一些 SVG 需要 45 分钟才能完全呈现在屏幕上，所以你可能想在手边准备一份点心。

如果你有兴趣帮助这个项目，听起来似乎[Kevin]可以使用一些帮助来找出为什么 Atari 1020 绘图仪不喜欢他的程序输出。如果您手边有 Turbo-BASIC XL 编程书籍，还有一些 SVG 函数和贝塞尔曲线形式需要做一些工作。

您是否需要在 Atari 1200XL 上查看 SVG 文件？不，可能不会。你可能也不想在 Macintosh SE/30 上玩 Spotify，但这并没有阻止黑客们想出你可以怎么做。只要这些旧机器还在运行，我们相信[社区会继续教他们新的技巧](https://hackaday.com/2018/04/08/orbital-mechanics-on-a-vintage-kaypro/)。