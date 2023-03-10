# 第四个模块有一根口香糖那么大

> 原文：<https://hackaday.com/2021/04/25/forth-module-the-size-of-a-stick-of-gum/>

澳大利亚工程师[John Catsoulis]开发了一个名为 scamp 2 的小模块，专门用于跑步。他的 Udamonic 项目的重点不仅仅是突出 Forth，而是制作一个易于使用并且不需要在你的计算机上安装任何 IDE 的模块。据该网站称，这些模块已经在教育以及产品开发的快速原型制作中找到了自己的位置。他的网站有一些好的资源，包括几个 Scamp/Forth 示例应用程序，如模型火车控制器或添加实时时钟模块。

该模块的核心是一个带有 64K Flash 和 8K RAM 的微芯片 PIC24F64GB202 MCU。其中，Forth 仅占用 20K 闪存和 2K RAM。[John]使用的是[flash Forth](https://flashforth.com)，这是大约十年前昆士兰大学的[Mikael Nordman]开发的 Forth 版本。FlashForth 已经在多种 PIC 和 AVR ATmega 处理器上实现，并且显然在澳大利亚和其他地方已经有了相当多的追随者。

我们从照片中估计，Scamp 大约 80 毫米长，比标准的 MIL-A-A-20175 A II 型口香糖(73 毫米)略长。您可以按原样使用它，或者在安装了接头引脚的情况下，Scamp 可以插入试验板以方便黑客攻击。关于 Scamp 与其他设备的接口，[John]说“编写软件来使用其他硬件是非常容易和有趣的。”我们喜欢他的态度。

这是来自他的 Hackaday.io 项目页面的更多信息，他还有一个 Tindie 网站，名为 T2。如果你想对在嵌入式系统中使用 Forth 有一个很好的了解，可以看看我们的 Forth 大师【埃利奥特·威廉姆斯】的 [*Forth:黑客的语言*](https://hackaday.com/2017/01/27/forth-the-hackers-language/) 。感谢[Stephen Walters]提供的提示。

 [https://www.youtube.com/embed/ojJI0Fbhyg8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ojJI0Fbhyg8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

