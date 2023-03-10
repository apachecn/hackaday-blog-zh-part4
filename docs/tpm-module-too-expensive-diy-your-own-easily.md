# TPM 模块太贵？轻松 DIY 自己！

> 原文：<https://hackaday.com/2022/05/04/tpm-module-too-expensive-diy-your-own-easily/>

自从 Windows 11 宣布其 TPM 模块要求以来，以前丰富且不受重视的 PC 主板 TPM 附加板的价格飙升。相反，我们一直在获取芯片并将它们焊接到我们自己设计的电路板上——而[【维克多】的项目](https://diy.viktak.com/2022/04/home-made-tpm2-0-module.html)是这方面的又一个例子。[Viktor]查看了他的 Gigabyte AORUS GAMING 3 主板的 TPM 模块的在线市场列表，发现它们的起价约为 150 欧元，几乎与主板本身的价格一样高。因此，和任何有自尊的黑客一样，他选择了 DIY 的方式，而且几乎没有遇到什么困难。

根据数据手册中的原理图，他很快制作了一个简单的 KiCad 布局，使其与主板用户手册中的引脚排列相匹配，然后从易贝订购了 PCBWay 和 SLB9665 芯片。两个都到达后，[viktor]组装电路板，并发现一个小错误-他设计了一个 2.54 毫米引脚接头的模块，但他的主板有 2.0 毫米接头。他连接了一个小适配器，使他组装的 1.0 版能够工作，并且安装了 Windows 11，没有任何 TPM 抱怨。他展示了他设计了一个新的 1.1 版本，也有一个更新的连接器，并在 GitHub 上为我们发布了它的(未经测试，但应该可以工作)设计文件[。这些模块可能会因制造商和主板系列而异，但随着每个模块的发布，一群黑客可以节省资金，并获得一个几乎可以保证成功的周末项目。](https://github.com/viktak/TPM-H370)

不管运行 Windows 11 的目标最终是否值得，它已经实现了。随着黄牛盯上了那些[只想把自己的硬件](https://hackaday.com/2021/06/29/the-great-windows-11-computer-extinction-experiment/)用于新操作系统的人，推出自己的 TPM PCB 是一个非常有吸引力的解决方案！上次我们报道了[一个用于 ASrock 服务器主板的 DIY TPM 模块，](https://hackaday.com/2022/04/06/build-a-tpm-module-for-your-server/)我们在评论中进行了生动的讨论，如果你想创建自己的 TPM 板，你可以去他们那里寻求建议和见解！