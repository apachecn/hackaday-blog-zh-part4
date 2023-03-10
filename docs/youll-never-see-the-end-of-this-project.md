# 这个项目你永远也看不到尽头

> 原文：<https://hackaday.com/2019/01/17/youll-never-see-the-end-of-this-project/>

不管怎样，理论上是这样的。当[奎因]幸运地发现一束 5 毫米红色发光二极管和一管 74LS164 移位寄存器时，一个项目跃入脑海:[“永远的数字”，一个周期比宇宙年龄还长的伪随机数发生器](https://hackaday.io/project/163034-the-forever-number)。当然，在序列重复之前，所用的组件早就失效了，但谁在乎呢，这东西看起来棒极了！

![](img/26d995cb9d79559814da8f7b0232691e.png)

Check out the gorgeous wire-wrapping job!

该项目的核心是一个由(31) 74LS164 构成的 242 位线性反馈移位寄存器(LFSR)。XOR 门和反相器通过对寄存器抽头上的两个反馈位进行 XNOR 运算来计算序列的下一位，然后将该位送入位 0。根据选择的反馈抽头，输出序列将在一定数量的时钟周期后重复，特殊的反馈抽头组给出的最大长度为 2^N–1，其中 N 是寄存器长度。我们在这里要注意的是，2 ^(242) 是一个很大的数字。

LFSR 的输出显示在 22×11 的 led 阵列上，产生的图案让人想起真实和虚构的复古超级计算机，如电影“战争游戏”中的 WOPR，或思维机器中的 CM2。

这个大规模移位寄存器的时钟来自——等等——一个 555 定时器。电位计允许在 0.5 至 20 Hz 范围内调整时钟频率，来自 XOR 和反相器 IC 的一些额外的门用作时钟分配缓冲器。

我们特别喜欢这个建筑。每个连接都在电路板背面小心翼翼地点对点缠绕，这是最初用于英特尔 SBC 80/10 系统的遗留物。这种类型的板前面有集成 DIP 插座，后面有绕线引脚，连接非常方便。没错，板上一滴焊料都没用。

休息之后，你可以在视频中看到 11 秒钟的图案。我们很高兴[奎因]没有拍摄整个序列，这将需要大约 22，410，541，156，499，040，202，730，815，585，272，939，064，275，544，100，401，052，233，911，798，596 年(假设时钟为 5 赫兹，并使用 241 和 171 位上的抽头)。

 [https://www.youtube.com/embed/ZCXPtg14aLo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZCXPtg14aLo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们推荐的另一个 LED/LFSR 黑客使用伪随机流来模拟闪烁的蜡烛。