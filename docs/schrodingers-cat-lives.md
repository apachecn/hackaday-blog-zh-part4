# 薛定谔的猫活着

> 原文：<https://hackaday.com/2019/06/10/schrodingers-cat-lives/>

如果量子物理学对你来说总是听起来有点古怪，振作起来。耶鲁大学的研究人员宣布，他们可以做到量子物理学声称不可能做到的事情:他们可以确定一个量子系统在崩溃前的状态。这与薛定谔著名的假设猫同时被叠加成 50%活着和 50%死了相矛盾。这项研究发表在[自然](https://www.nature.com/articles/s41586-019-1287-z)杂志上。

薛定谔认为，在你打开盒子之前，猫是半死不活的，就像一个量子位可以处于一种或另一种状态的 50%一样。当你观察它时，你强迫系统进入一种状态。然而，耶鲁大学的研究人员已经找到了一种方法，利用微波间接监控量子位，在系统跳跃之前确定它们的状态。不像正常的观察发生得太晚，耶鲁技术允许研究人员改变他们选择的未来状态。

正如你所料，看到量子跳跃的开始需要相当多的实验设置，并采用 FPGAs，这并不奇怪。不过，它的核心是一个简单的 LC 振荡器。振荡器以大约 9 GHz 的频率发射，频率根据量子位的状态而变化。

看看物理学界是否能重现这一点，以及它是否会给量子理论带来任何重大变化，这将是一件有趣的事情。特别是，这可能会对实用的[量子计算](https://hackaday.com/2018/01/24/quantum-weirdness-in-your-browser/)产生深远的影响，这是我们去年讨论过的一个话题。现在我们只需要黑掉[肖恩·博伊斯的][量子咖啡机](https://hackaday.com/2019/04/01/schrodinger-quantum-percolator-makes-half-decent-coffee/)。