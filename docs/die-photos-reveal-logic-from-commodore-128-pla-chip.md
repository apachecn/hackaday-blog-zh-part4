# 模具照片揭示了 Commodore 128 PLA 芯片的逻辑

> 原文：<https://hackaday.com/2020/07/29/die-photos-reveal-logic-from-commodore-128-pla-chip/>

8721 PLA 或可编程逻辑阵列是使 Commodore 128 成为现实的芯片之一，Commodore 128 是形成早期个人电脑革命前沿的最后一种 8 位计算机。约翰·格里普得到了其中一个芯片，[决定对其进行逆向工程](https://c128.se/posts/silicon-adventures/)，看看 C-128 设计师在 20 世纪 80 年代中期的想法。

PLA 是当时的 FPGAs，带有与门和或门的阵列，可以连接成复杂的逻辑电路。[Johan]的调查从将 8721 芯片从其包装中取出开始，为此他使用了[CuriousMarc]喜欢的[快速简单的方法](https://hackaday.com/2020/03/11/chip-decapping-the-easy-way/)。下一步是装配工具，因为他使用的显微镜不足以完成这项任务。即使手里有了更好的显微镜，[Johan]仍然发现有必要对它进行调整，增加一个新的高质量的 Raspberry Pi 相机，并用一些步进电机和一个 CNC 控制器板来实现舞台的机动化。

光学分类后，他能够识别芯片上的所有焊盘，并找到主要的门阵列区域。再放大一点，他能够看到“与”和“或”门矩阵之间的联系，这使得解码逻辑变得相对容易，尽管看起来像是具有锁存功能的输出块的存在在某种程度上混淆了这一点。

最终结果是一个完整的 Verilog HDL 文件，它反映了原始的 8721 逻辑，我们认为这是一个非常巧妙的技巧。如果我们自己的[Bil Herd]能在这一点上附和，我们会很高兴；毕竟是他[从字面上设计了 C-128](https://hackaday.com/2013/12/09/guest-post-the-real-story-of-hacking-together-the-commodore-c128/) 。