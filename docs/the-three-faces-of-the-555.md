# 555 的三面

> 原文：<https://hackaday.com/2019/04/03/the-three-faces-of-the-555/>

在这些廉价微控制器的日子里，很难记得曾经有一段时间计时需要真正的电路。即使在今天，对于一些应用来说，很难击败无处不在的 555 定时器 IC。它便宜、丰富、可靠。555 的有趣之处在于，与其说它是一个专用芯片，不如说它是一个芯片上的一堆构建模块。你可以用不同的方式将这些积木连接起来，以获得不同的效果,[ learne electronics]有一个视频展示了你通常在 555 上看到的三种主要模式:非稳态、双稳态和单稳态。

555 实际上只有几个比较器、一个分压器、一两个晶体管、一个触发器和一个反相器。想法是你用一个电容充电，比较器可以用不同的方式设置或复位触发器。复位输入或触发器可以接通晶体管，使电容器放电。

非稳态模式只产生一系列脉冲。双稳态模式实际上只是暴露了内部触发器。单稳态通过产生固定的输出脉冲对输入做出反应。当然，你可以让 Arduino 或其他微控制器来做所有这些，但代价是复杂性。

我们有很多 555 个[项目](https://hackaday.com/2017/12/13/the-tiniest-of-555-pianos/)，有些相当[独特](https://hackaday.com/2017/05/08/conflict-escalates-between-brilliant-rat-and-555-timer/)。我们也看了这个古老芯片的[历史](https://hackaday.com/2018/10/10/the-555-and-how-it-got-that-way/)。

 [https://www.youtube.com/embed/pPP8wadZ2Rk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pPP8wadZ2Rk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

