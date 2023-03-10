# 从腐蚀性死亡中拯救您的原始 Xbox

> 原文：<https://hackaday.com/2020/12/14/save-your-original-xbox-from-a-corrosive-death/>

8 位和 16 位时代的复古电脑粉丝们会很清楚从里到外吃掉这些机器的绿色死亡。一个常见的原因是电解电容泄漏，当腐蚀破坏主板时，RTC 电池甚至是一个更邪恶的祸害。当然，随着时间的推移，新一代机器现在容易出现这种风险。[[MattKC]在微软 2001 年至 2009 年生产的原始 Xbox 上探讨了这个问题。](https://www.youtube.com/watch?v=uy-btflp0-U)

![](img/3b92e6e3f2647b9d445241f7a829ae6e.png)

Despite looking okay from above, the capacitor inside the Xbox had already started leaking underneath. Leaving this in the console would inevitably cause major damage.

最初的 Xbox 确实包括一个实时时钟，但是，它不依赖于电池。由于 RTC 硬件包含在更大的 NVIDA MCPX X3 声音芯片中，待机电流太高，无法使用标准硬币电池作为备用电池。取而代之的是，使用了一个奇特的高值电容器，使时钟在没有交流电源的情况下维持几个小时。问题是[这些电容器是在 21 世纪初的电容器瘟疫期间制造的。](https://en.wikipedia.org/wiki/Capacitor_plague)随着时间的推移，它们会泄漏并在主板上沉积腐蚀性物质，这很容易杀死 Xbox。

解决办法？移除电容器并清除可能已经留在电路板上的任何粘性物质。挑剔的人可以更换零件，尽管 Xbox 没有电容器也能正常工作；你只需要在每次拔掉控制台的时候重置时钟。[MattKC]还指出，现在是检查电路板上其他电容是否存在有害泄漏的好时机。

我们以前见过[MattKC]潜入控制台，从网上找到的源代码中烧他自己的 PS1 modchip。休息后的视频。

编辑:正如[Doge Microsystems]所指出的，这个灾难只影响 1.6 之前的 Xboxes 后来的型号没有同样的问题，不应该这样修改。

 [https://www.youtube.com/embed/uy-btflp0-U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uy-btflp0-U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

