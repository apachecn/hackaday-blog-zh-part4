# 俄罗斯方块钟

> 原文：<https://hackaday.com/2019/06/13/a-tetris-clock/>

这些年来，我们从来不缺少时钟项目，这个项目很有趣，因为它使用俄罗斯方块风格的积木拼出来的时间。这个项目看起来不错，适合不同的显示器。代码在 GitHub 上，它依赖于一个俄罗斯方块库，该库已被更新为处理不同的显示，甚至 ASCII 文本。

[Brian]想要为时钟使用 ESP8266 开发板，但该库有一个错误，使其无法工作，所以他使用了 ESP32 板。该板是 TinyPICO，有一个分线板，与显示器配合良好。

还有一些腿的 3D 打印小部件。如果我们诚实的话，我们会说这个项目看起来很酷，但技术不是革命性的。我们发现有趣的是，这是一个很好的例子，说明了开源是如何建立在自身之上的。

当然，图书馆做了大量的工作，但是根据[Brian]的说法，它有几个作者。[Tobias Bloom]开始编写代码，其他人已经修改了库，以绘制 ASCII 字符并支持任何使用 AdaFruit GFX 风格库的显示。

因此，虽然代码很简单，但结果却令人印象深刻，这是[Brian]利用他人大量代码的结果——这是一个开源实践的很好的例子。

我们研究了 Brian 使用这个库作为 YouTube 订阅计数器的情况，但是我们认为时钟有更普遍的吸引力——不是每个人都有很多 YouTube 订阅者。如果你没有生活，你可以试着用生活游戏重新制作[俄罗斯方块](https://hackaday.com/2017/09/17/building-a-working-game-of-tetris-in-conways-game-of-life/)。

 [https://www.youtube.com/embed/ey2mjZ-UQNM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ey2mjZ-UQNM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

