# ISASTM 通过 USB 运行复古卡

> 原文：<https://hackaday.com/2020/10/16/isastm-runs-vintage-cards-over-usb/>

ISA 总线是遥远过去的遗迹，不再受 PC 主流的支持。除了复古狂热分子和一些长期工业用户，它几乎被遗忘了。然而，这并没有阻止[Manawyrm]继续进行黑客攻击，而且他已经为现代开发了一个漂亮的适配器。

ISASTM 仍处于早期开发阶段，它是一种 ISA-over-USB 适配器，允许现代计算机与旧的扩展卡一起工作。[运行在 STM32H743 上，](https://www.vogons.org/viewtopic.php?p=902486#p902486)使用微控制器的本机 USB1 接口，ISASTM 卡能够插入背板，以便用一个适配器寻址多个卡。[Manawyrm]通过在 PCem 仿真器[中运行猴岛 1 来演示硬件，声音由 AdLib ISA 声卡](https://twitter.com/Manawyrm/status/1316416815598317569)提供。

有一些吞吐量问题，[Manawyrm]旨在通过切换到 USB2 并对代码进行一些调整和改进来解决这些问题。无论如何，这是一个令人印象深刻的工具，我们认为它也可以用来保存一些遗留的硬件。顺便说一句，我们已经很久没有在这些地方看到可靠的 ISA 黑客了。休息后的视频。

 [https://www.youtube.com/embed/5jW1dGRhmsE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5jW1dGRhmsE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢 tsys 的提示！]