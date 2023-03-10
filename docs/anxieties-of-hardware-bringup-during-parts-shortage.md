# 零件短缺时硬件带来的焦虑

> 原文：<https://hackaday.com/2022/05/04/anxieties-of-hardware-bringup-during-parts-shortage/>

[Dirksavage88]给我们讲述了一个在芯片短缺的时候[开发简单 BEC 的故事。](https://hackaday.io/project/185199-800-power-module-put-to-good-use)他需要一个 5V/3A 的小型调节板用于无人机上的伺服轨道，并决定使用德州仪器的一种新型集成电感模块。几乎不需要任何外部零件，这种模块非常适合用于所有的电源轨需求，尽管成本略有增加-缺点是，随着零件短缺的到来，大多数都已经缺货。这些特定模块 LMZM33603 最初的定价约为 7 美元，现在的要价已经攀升至 800 美元。不管怎样，他还是获得了一些这样的模块，并继续设计电路板。

测试你的第一个 PCB 可能会很困难，因为你放在上面的硅片对你的目的来说是不可替代的。TI 以其古怪的足迹而闻名，该模块也不例外-焊膏应用需要一点时间，回流后看到模块周围的小焊球并没有让他完全放心。值得庆幸的是，当他给它加电时，这个模块创造了奇迹，并在他的无人机伺服转台中占据了它应得的位置。他说，我们可以期待他的设计在 2024 年的下一次修订，或者是据报道的 100 周交付时间到期的任何时候。如果我们中的一些人可以使用它们，在 GitHub 上可以得到 Eagle 文件！

我们中有相当多的人足够幸运，拥有足够的关键部件来满足我们的需求，但我们中的大多数人都将一些项目搁置到更好的时候——比如这个支持 WiFi 的墙上充电器项目。甚至更大的项目也受到了影响，从[滑冰板](https://hackaday.com/2021/07/17/tales-from-the-global-chip-shortage-smoothieboard/)到[树莓派。](https://hackaday.com/2022/04/08/its-almost-a-new-raspberry-pi-compute-module-4-but-not-quite/)就在一年前，我们[让读者分享了他们的芯片短缺故事。](https://hackaday.com/2021/05/24/ask-hackaday-how-is-the-chip-shortage-affecting-you/)

 [https://www.youtube.com/embed/8lK-6-G_LNE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8lK-6-G_LNE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

