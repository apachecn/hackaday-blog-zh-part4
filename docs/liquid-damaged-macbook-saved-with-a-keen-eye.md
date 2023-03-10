# 敏锐的眼光挽救了液体损坏的 MacBook

> 原文：<https://hackaday.com/2019/07/09/liquid-damaged-macbook-saved-with-a-keen-eye/>

即使在我们这些有修理电子产品嗜好的人中，也有一些失败被普遍认为太严重而无法挽回。笔记本电脑中的液体损坏就是一个很好的例子；如此多的元件和复杂的电路挤在如此小的区域内，一旦腐蚀开始，搞不清楚是什么是真正的噩梦。尤其是对于一台旧的笔记本电脑，传统的想法是尝试恢复你的文件，然后买一台新的。

但正如我们逐渐了解到的，[杰森·金]并不是一个经常发现自己与传统智慧有关联的人。在发现一台怀疑有液体损坏的旧 MacBook 后，[他决定看看如何才能让它恢复正常工作](https://ripitapart.com/2019/07/07/resurrecting-a-dead-macbook-pro-mid-2012-13-inch-model-a1278/)。根据设备上的说明，屏幕没电了，USB 端口烧坏了，电池没有充电，也无法启动。没问题，应该很容易。

[![](img/ff7bab84ddb51dfa1f95c0f11f1d8296.png)](https://hackaday.com/wp-content/uploads/2019/07/macbookrepair_detail.jpg) 打开大约 2012 年的笔记本电脑，【杰森】发现机器已经被腐蚀得千疮百孔。我们也不仅仅是在谈论表面粘糊糊的东西。用异丙醇彻底清洗后，损坏的真实程度就清楚了。不仅印刷电路板上的痕迹腐烂了，而且还有许多组件被损坏或完全丢失。不管溅到这个可怜的苹果里面的是什么，很明显是一些肮脏的东西。

[Jason]使用 OpenBoardView 调出主板的原理图和图表，并开始将它们与他损坏的单元进行视觉比较的艰巨任务。在某些区域，腐蚀非常严重，他仍然很难找到正确的轨迹和焊盘。但随着时间和努力，他能够开始四处探查，看看哪些组件实际上放弃了幽灵。

对于 USB 端口，它最终是一个坏的 10 微法陶瓷电容器，但对于 LCD，他最终不得不更换整个背光驱动器 ic。在这个小小的 BGA-25 器件上工作的前景可能足以让一些人认输，但与电路板上其他地方所需的手工焊接磁线修复相比，[Jason]说，新 LP8550 芯片的安装是整个操作中较容易的一个方面。

如果你喜欢一个好的修复成功故事，这篇文章是一个很好的读物，我们尤其喜欢他在每个系统的基础上记录他的诊断和结果工作的方式。这让我们更容易理解[杰森]到底要扑灭多少场火灾。但是，如果你对稳定焊接的技艺更感兴趣，[看看他最近的项目，为 Atomic Pi](https://hackaday.com/2019/06/26/how-do-you-get-pci-e-on-the-atomic-pi-very-carefully/) 添加一个 PCI-E 插槽。