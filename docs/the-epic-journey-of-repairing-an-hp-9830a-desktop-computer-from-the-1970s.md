# 维修 20 世纪 70 年代惠普 9830A 台式电脑的史诗般旅程

> 原文：<https://hackaday.com/2022/04/18/the-epic-journey-of-repairing-an-hp-9830a-desktop-computer-from-the-1970s/>

我们喜欢 Hackaday 的复古电脑，我们总是很高兴看到有人从垃圾填埋场抢救出一件历史文物。有时，只需要更换一个损坏的电源开关或漏电的电容器；其他时候，你需要拿出示波器，深入研究内部电路。但是，让惠普 9830A 重新站起来所做的大量工作是你不常看到的。

如果你不熟悉 HP 9830A，它是一台 20 世纪 70 年代早期的台式电脑，完全由分立逻辑门构建而成。[Jerry]桌子上的机器完全停止了运转，甚至连风扇都不转了。这是由一个不可靠的电源开关引起的，但更换开关只是开始:电源内部有几个坏的组件，主板背面有大量潮湿的灰尘。在彻底清洁和更换几个故障组件后，所有四个电源轨再次在规格范围内运行。

接下来是调试组成 CPU 的四块印刷电路板的复杂任务。[Jerry]将他的逻辑分析仪连接到这些主板上，以可视化 CPU 在通过微码时的内部状态。同样，几个 TTL 芯片被证明是坏了，需要更换。随着 CPU 的工作，是时候进入主程序 ROM 了，这最终消耗了[Jerry]大量的修复时间。

损坏的 ROM 芯片的问题不在于找到替代品，而在于获得其内容的正确副本。幸运的是，有一个周期精确的 HP 9830a 仿真器，其中包含整个固件的副本。随着几十个 ROM 芯片中的几个出现问题或损坏，修复原来的 ROM 板是不现实的，所以[Jerry]设计了一个完整的替代板。有了一个现代的，可重新编程的 EPROM 芯片和一些胶合逻辑，这也是一个巨大的帮助，因为它允许他在计算机上运行定制的机器代码。

[![A PCB with an EPROM chip and some glue logic](img/0fd2b2ca64a5bb9c6f8a4acada403a04.png)](https://hackaday.com/wp-content/uploads/2022/04/HP9830A-Replacement-ROM-Board.png)

The replacement ROM board contains just one EPROM and some decode logic.

通过将一些测试程序写入 EPROM [Jerry]能够测试所有的 RAM、ROM 和寄存器以及显示器，并发现更多损坏的芯片需要更换，错误的连接需要修复。随着所有主要功能的运行，HP 9830A 再次恢复生机并响应命令。唯一剩下的问题是磁带机，结果是由传感器损坏引起的。一旦被替换，修复过程最终完成。

[Jerry]对他的 26 集视频系列的连续评论对计算机体系结构的复杂性给出了许多很好的见解，所以如果你正在寻找一些可以疯狂观看的东西，忘记网飞，放上[Jerry]的视频。它们还显示了系统故障排除方法的重要性:从最基本的系统开始，验证它是否完全按照预期工作，然后才开始添加其他组件。

如果你不能得到足够的老式惠普齿轮修理，检查相关的惠普 9825 的[这个修理。正在进行的](https://hackaday.com/2021/05/19/repairing-a-vintage-hp-9825-the-hard-way/)[修复百夫长小型计算机](https://hackaday.com/2022/03/20/minicomputer-restoration-hanging-in-the-balance/)的过程也绝对值得关注。

感谢提示，[mgsouth]！

 [https://www.youtube.com/embed?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLzvLbUxGuZ-zv0jpoUe048ecMPVAJiPDA](https://www.youtube.com/embed?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLzvLbUxGuZ-zv0jpoUe048ecMPVAJiPDA)

