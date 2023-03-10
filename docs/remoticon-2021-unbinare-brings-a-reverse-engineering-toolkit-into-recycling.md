# Remoticon 2021: Unbinare 将逆向工程工具包引入回收领域

> 原文：<https://hackaday.com/2022/01/06/remoticon-2021-unbinare-brings-a-reverse-engineering-toolkit-into-recycling/>

Unbinare 是一家比利时小公司，与回收和翻新公司合作，站在将电子垃圾转化为有用物质的前沿。逆向工程是一种实现回收的新方法，但它可能是最有前途的方法之一，我们还没有大规模尝试。在 Hackaday Remoticon 2021 上，Maurits Fennis 谈到了 Unbinare 在该领域的努力，并向我们展示了他最近发布的一个工具包，作为他工作的一部分，并描述了他作为艺术家的背景如何给他带来了用于制定 Unbinare 基本原则的见解。

Unbinare 的工具被设计成彼此协调工作，这是任何高效逆向工程工作的一个要求。喂！STER 是一个通用的回收 MCU 研究板，带有插槽以适应不同的 TQFP 芯片尺寸。该板是 Maurits 在逆向工程方面的经验浓缩成的通用工具，包括用于不同编程/调试接口的无数连接器。我们不知道该板的完整范围，但照片显示 TQFP 插座内有一个 STM32 芯片，除了你选择的在线零售商外，到处都有。除了所有的方法打破引脚，喂！STER 有电源和时钟故障的插座，让你用 ChipWhisperer 这样的工具瞄准这两个无处不在的致命弱点。

没有像 OI 这样的工具！斯特独自一人。UNBRK 是一个分线板，用于更永久和定制的反向工程夹具，其走线和电源层布局复杂，具有无与伦比的通用性，可重复使用各种 IC。即使使用专门制造的夹具，对各种信号的专门探测仍然是必须的，UNBProbe 是一种测试点探针，带有可选的漂亮的 3D 打印外壳，设计时考虑了可用性和独立组装的方便性。一旦你在一个项目中使用了太多这样的探针，你肯定会想要为自己建立一个 UNBProbeBase，一个将一堆 UNBProbeBase 组合到一个舒适的连接器中的母板——否则，电缆会扩展到占据所有可用的空间，分散你对今天的 RE 难题的注意力，并打扰你进行不请自来的拓扑练习。

无论是以回收为目的的黑客攻击，还是简单地释放你的设备来做你想做的事情，Unbinare 的工具都是有用和漂亮的，这项工作扩展到其他资源，如记录他们的努力和分享工具设计的维基页面。如果你想随时了解他们的下一个里程碑，你最好的选择是[在 Twitter](https://twitter.com/unbinare) 上关注他们，因为无论何时下一个工具和项目公告发布！

 [https://www.youtube.com/embed/zE7b9tZB2eo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zE7b9tZB2eo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

