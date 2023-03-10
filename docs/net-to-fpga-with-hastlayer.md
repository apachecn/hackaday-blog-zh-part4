# 。使用 Hastlayer 从网络到 FPGA

> 原文：<https://hackaday.com/2019/12/15/net-to-fpga-with-hastlayer/>

有很多方法可以使用 FPGAs。一种方法是将计算相关的软件转换成硬件。这可以提高速度，在某些情况下还可以降低功耗。通常，你可以通过编写 C 的子集来实现，但是[has layer](https://hastlayer.com/)可以转换。NET 程序集集成到 FPGA 配置中，但有一些限制。

Hastlayer 背后的匈牙利公司声称，他们最终将不得不为某些东西收费，但目前，该工具是免费的，他们承诺将始终有一些免费的选项。有趣的是。NET 程序集本质上是目标代码，所以你不是在编译源代码，而是一种可以用许多不同的语言工具生成的中间语言。

实际的编译发生在远程服务器上，所以有些人不会喜欢这样。然而，至少你没有加载你的源代码，只有 dll。该工具的目标是 Nexys 4 DDR 板，现在显然是 Nexys A7 板。该板仅售 265 美元，但坦率地说，对于你通常想用 FPGA 加速做的事情来说，它有点贫血。在入门指南中，他们甚至说:

> 请注意，这是一个相对低端的开发板，无法适应巨大的算法，它只支持缓慢的通信通道。所以用这个板 Hastlayer 只适合于比较简单的算法，只需要交换少量的数据。

据推测，他们最终会支持更大的硬件。

当然，这也有局限性。只有公共虚方法或实现接口中定义的方法的方法才会有硬件入口点。并非所有数据类型都可用。一些像数组的方法。副本功能有限。没有例外，递归也有一些限制。

不过，如果你擅长。NET，并希望进入 FPGA 协同处理，这可能只是事情。如果你更喜欢 C，有一个工具可以帮你实现这个目标。或者也许你更喜欢 [Python](https://hackaday.com/2012/06/13/myhdl-python-programming-option-for-fpga/) 。