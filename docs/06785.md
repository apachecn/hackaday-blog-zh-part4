# 测量时间是一件轻而易举的事

> 原文：<https://hackaday.com/2020/06/25/measuring-the-time-is-a-breeze-with-this-air-flow-clock/>

如果你曾经做过手术，并且你已经过了一定的年龄，那么你很有可能熟悉可怕的激励肺活量计。这是一个有一根或多根柱子的小塑料装置，每根柱子里都有一个塑料球。这个想法是向这个东西吹气来使球漂浮，以确保你的肺部保持良好的状态，减少肺炎的机会。这个独特的气动时钟让我们想起了那个装置，却没有所有的痛苦。

像肺活量计一样，[Nir Tasher]的时钟有三个校准过的管子，每个都足够大，可以宽松地容纳一个泡沫球。在每根管子的底部是一个鼓风机，其电机由 PWM 控制。一个激光测距仪坐在每个球的下面，测量它的高度；PID 回路使用该测量来控制每个风扇的速度，从而控制每个球的高度。下面的视频显示，球实际上相当稳定，使时钟容易阅读。然而，它没有揭示时钟的声音是什么样的；我们要大胆地猜测一下，这里一定很吵。尽管如此，我们认为这是一种非常棒的计时方式，而且是独一无二的。

[Nir]的气流时钟是地球上最大的硬件设计竞赛[2020 年 Hackaday 奖](https://prize.supplyframe.com/)的早期参赛作品。每个人都应该参与一些事情，或者至少看看[人们用](https://hackaday.io/submissions/prize2020/list)想出的酷东西。现在还处于过程的早期，但是已经有这么多优秀的项目了。你还在等什么？

 [https://www.youtube.com/embed/eGN-MeLun5U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/eGN-MeLun5U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2020](https://prize.supplyframe.com) is Sponsored by:[![Supplyframe](img/193ca31946d20fcfa39296cb816a4c50.png)](https://supplyframe.com/)[![Digi-Key](img/4fc24a8a6b4498aecfe987b00009d192.png)](https://www.digikey.com/)[![Microchip](img/8dd361210bbb0e5592c24f87e4e2267e.png)](https://www.microchip.com/)[![Arm](img/7d728b281b85469ef9013d45001f14b4.png)](https://www.arm.com/)