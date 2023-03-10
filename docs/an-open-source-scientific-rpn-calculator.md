# 一个开源的科学 RPN 计算器

> 原文：<https://hackaday.com/2021/06/05/an-open-source-scientific-rpn-calculator/>

当您使用一个在计算中使用 RPN(反向波兰符号)的模型，并且同时是一个定制版本时，为什么要使用一个平淡无奇的商用计算器呢？孩子们可能有彩色薄膜晶体管和图形功能，但你的键盘没有等号，那*意味着*什么的。

不幸的是，对于 RPN 爱好者来说，RPN 计算器有点少见。由于 20 世纪 70 年代和 80 年代的经典模型相当昂贵， [[ 安东·波洛克托夫 ]只是建立了自己的 OpenCalc](https://hackaday.io/project/179949-openrpncalc) 。这个辉煌的标本是一个开放的硬件 RPN 计算器，其设计不仅仅是对古老的惠普 HP42 的认可。

它的核心是一个 STM32L476 低功耗 ARM 处理器和一个夏普内存 LCD，所有这些都在一个 3D 打印外壳中的 PCB 上，这在 20 世纪 80 年代是你引以为豪的。它运行在 CR2032 上，这比一些现代风格的计算器更好，它给用户提供了你在科学计算器中所希望的一切。关键的图例是一组可打印的标签，当打印在自粘激光薄膜上时，证明足够耐用。所有的资源都可以在 GitHub 库中找到[，所以如果 RPN 是你的东西，没有什么可以阻止你为自己建立一个。](https://github.com/apoluekt/OpenRPNCalc)

如果你对 RPN 感兴趣，[这是一个我们在过去已经详细讨论过的主题](https://hackaday.com/2017/10/24/reverse-polish-notation-and-its-mildly-confusing-elegance/)。