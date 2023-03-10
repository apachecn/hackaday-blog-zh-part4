# 那些 NES DIP 芯片是如何被简化为 qfn 的

> 原文：<https://hackaday.com/2022/11/07/how-those-nes-dip-chips-were-reduced-to-qfns/>

控制台改装的世界让我们看到了一些令人印象深刻的项目，最近我们特别提到的一个项目是由[Redherring32]生产的便携式 NES。它很特别，因为最初的 NES 定制 DIP 芯片已经被打磨成类似表面贴装 QFN 封装的东西。当我们的同事[Arya]写下这个项目时，没有太多的信息，但从那时起，全部细节[已经放在了 GitHub 的知识库](https://github.com/Redherring32/TinyTendo)中。也许最有趣的是，它包括了[一个芯片打磨过程的完整教程](https://github.com/Redherring32/TinyTendo/wiki/Chip-Trimming-Guide)。

要拿不可替代的经典芯片去打磨，肯定需要一些胆量，但前提是足够健全。DIP 封装内部是一个芯片载体和一个连接引脚的接触片网，这一过程只需打磨掉环氧树脂，露出这些接触片用于新的接触。然后，结果可以像任何 QFN 一样进行重排，并用于一个新的、更小的 NES。

在这一过程中，这提供了一个我们大多数人从未见过的对 DIP 结构的迷人见解。如果你们中的任何一个人曾经设法将一个引脚从 DIP 上拉下来，那么毫无疑问，你们也会想如何将这项技术用于重新连接导线。

你可以在这里阅读我们对该项目的原始报道。