# 使用 SprintLayout 对 PCB 进行逆向工程

> 原文：<https://hackaday.com/2019/12/31/reverse-engineer-pcbs-with-sprintlayout/>

[b back]有一些旧 Commodore 卡的扫描照片，想用它重新制作 PC 板。的确，他本可以在 CAD 软件包中手工重画所有的东西，但这很乏味。相反，[他使用了 SprintLayout 6.0](https://www.youtube.com/watch?v=g0nkLJ4YQ2c) ，它允许你导入图片，并使用它们作为重新创建 PCB 布局的指南。

你可以看到整个过程，包括拉直原始扫描。有一些工具可以非常容易地在原始扫描图像上放置新的结构。

有人可能会认为这个过程可以更加自动化，但看起来好像每个部分都需要至少触摸一次，但这仍然比试图一起观察所有部分更容易。

大部分视频都是加速的，这让他看起来真的很快。你的速度会慢一些，但是从扫描到合理布局还是相当快的。

这个软件不是免费的，但是你可以在 KiCAD 中做一些类似的事情。诀窍是将图像完美缩放，并将其转换为用户层上的组件。然后，您可以添加新组件，并使用户层能够在您工作时看到图像。甚至还有一个在 KiCAD 中重建的旧电路板库。

可能有无数种方法来解决这个问题。旧版本的 SprintLayout 对 [Re-Amiga 1200](https://hackaday.com/2018/08/28/recreating-the-amiga-1200-pcb-from-pictures/) 有所帮助。

 [https://www.youtube.com/embed/g0nkLJ4YQ2c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/g0nkLJ4YQ2c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

