# 通过将机器视觉添加到 3D 打印机来解决 Wordle

> 原文：<https://hackaday.com/2022/02/26/solving-wordle-by-adding-machine-vision-to-a-3d-printer/>

说实话，我们还没有赶上这股潮流，主要是因为我们不需要被提供另一种消遣——我们完全有能力找到自己的兔子洞掉下去，非常感谢。但是字谜看起来确实很吸引人，因为规则和界面都很简单，难怪我们最近看到了一些像[这种自动化的 *Wordle* 解算器](https://www.reddit.com/r/raspberry_pi/comments/sxy31u/raspberrypi_wordle_robot/)这样的努力。

*Wordle* 的目标是在尽可能少的猜测中找到一个特定的五个字母的或多或少常见的英语单词。每个回合都以字母颜色编码的形式给出线索，以表明它们是否出现在单词中以及以什么顺序出现。[iamflimflam1]的方法是在 3D 打印机的底座上安装一个 Raspberry Pi 摄像头，并在打印头的位置安装一个手机触控笔。运行 *Wordle* 的手机被放置在打印机床上，打开 CV 用于查找手机屏幕以及手机在打印机床上的位置。从那里，机器人用手写笔输入一个开始的单词，分析盒子的颜色，并缩小解决方案的范围。

下面的视频展示了正在使用的机器人，如果你想亲自尝试，可以从获得[源代码。如果你需要更深入地研究*文字游戏*的求解算法，以及*dle 领域的其他变体谜题，可以看看](https://github.com/atomic14/wordle_robot)[最近这篇关于对流行游戏](https://hackaday.com/2022/02/08/wordle-reverse-engineering-and-automated-solving/)进行逆向工程的文章。

 [https://www.youtube.com/embed/_QHz_5pqPuo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_QHz_5pqPuo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[基因]的提示。