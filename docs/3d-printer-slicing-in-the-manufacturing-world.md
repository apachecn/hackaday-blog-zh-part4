# 制造业中的 3D 打印机切片

> 原文：<https://hackaday.com/2022/10/29/3d-printer-slicing-in-the-manufacturing-world/>

众所周知，你在车库里制造东西的方式很少是大公司大规模制造东西的方式。但有时生产车间的新技术会泄露给爱好者，反之亦然，所以留意对方在做什么是值得的。也许这就是 Carolyn Schwaar 在 All3DP 上发表的题为“[超越 Cura 切片器:专业 3D 打印构建准备软件](https://m.all3dp.com/1/beyond-cura-slicer-3d-printing-build-prep-software-for-pros/)”的帖子背后的想法在这本书里，她看了一些商业级 3D 打印机用于切片的程序。

我们通常使用的软件和那些旨在与专用高端机器一起工作的软件之间的差异非常明显，但可能不是以你所期望的方式。虽然您可能希望它们与目标机器紧密集成，但是您可能没有想到它们通常比像 Cura 这样的产品提供的参数控制更少。正如帖子中引用的那样，Cura 有超过 400 个设置。商业 3D 打印机没有时间无休止地调整这些设置。因此，重点更多的是放在可以工作的固定档案上。

然而，并不是所有的程序都与机器相关联。商业 CAD 产品对 3D 打印机的处理能力越来越强，有时可以将作业切片并直接发送给打印机。不管软件类型如何，每个人都需要某些功能:设计、修复、模拟、构建板布局等等。

如果你正在寻找除 Cura 之外的业余爱好级切片器，我们一直在使用 [SuperSlicer](https://hackaday.com/2021/10/26/superslicer-reviewed-another-3dp-slicer/) ，它是 [PrusaSlicer](https://hackaday.com/2019/05/24/3d-printering-the-past-and-future-of-prusas-slicer/) 的一个分支，后者是 Slic3r 的一个分支。