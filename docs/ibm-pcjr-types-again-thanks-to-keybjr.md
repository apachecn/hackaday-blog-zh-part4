# IBM PCjr 再次打字，感谢 KeybJr

> 原文：<https://hackaday.com/2022/04/24/ibm-pcjr-types-again-thanks-to-keybjr/>

我们大多数人认为键盘——即使是老式键盘——是相当标准化和可互换的，但 IBM PCjr 并非如此。它的键盘与当时的大多数键盘都不一样，这意味着没有原装键盘的 PCjr 就像一个吸尘器。正是这一点促使[Jozef Bogin]创造了 [KeybJr](http://boginjr.com/it/hw/keybjr/) ，这是一种硬件，允许人们在 IBM PCjr 上使用任何 at、XT 或 PS/2 键盘。

[![](img/9611a0b7b916f319c21d46fc96bd637a.png)](https://hackaday.com/wp-content/uploads/2022/04/pcjr-3.jpg)

The PCjr’s oddball keyboard can be a bit of a hassle for vintage computing enthusiasts.

PCjr 的键盘有什么奇怪之处？从外面看起来很正常，但它肯定有自己的事情在进行。首先，PCjr 键盘的操作协议与当时的其他键盘完全不同。此外，它与主机的连接要么是通过 IR，要么是通过它自己的有线电缆适配器。

KeybJr 通过使用基于 Arduino 的电路板来解决这个问题，将当时其他键盘的输入转换为 PCjr 期望的东西。这些信号通过红外线或有线键盘链接的 PCjr 的“K”端口发送和接收。

为什么要为 IR 功能费心呢？嗯，PCjr 上的连接器和引脚不是很坚固，有时会损坏。在这种情况下，可以选择通过 IR 链接使用普通的(当时的)键盘。毕竟，古董五金并不总是完美无缺的。这就是为什么像 PCjr 的 [ATX 电源适配器](https://hackaday.com/2018/09/10/atx-adapter-for-the-ibm-pcjr-now-available/)这样的东西存在。

想试试吗？KeybJr 有一个 GitHub 库，你可以在下面的一个简短视频中看到它的运行。

 [https://www.youtube.com/embed/Bb4gKPUSRpY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Bb4gKPUSRpY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

