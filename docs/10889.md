# 3D 打印机自动换床系统从杂志加载

> 原文：<https://hackaday.com/2021/08/03/3d-printer-automated-bed-swapping-system-loads-from-a-magazine/>

FDM 3D 打印已经超越了原型制作，被许多公司用作生产工具。然而，传统的打印机仍然需要操作来弹出床的完成部分并开始新的打印。[Thomas Sandladerer]想要一种无需人工干预的换床方式，所以[他建造了一个自动打印表面更换系统](https://www.youtube.com/watch?v=8O9E9rcH6Us)。

这个问题最显而易见的解决方案可能是像 Creality CR-30 这样的带式打印机，但这些打印机也有一些权衡。床粘附可能是一个问题，缺乏刚性的印刷表面会导致某些部分翘曲。[Thomas]希望能够使用 PEI 涂层钢床来避免这些问题。他的解决方案是一个从“杂志”中拉出床的系统，并在一部分完成后推出旧床。它仍然使用磁性加热床，在改变印刷表面之前降低。每个打印表面都安装在一个 3D 打印框架内，该框架位于刀具更换框架上，并在加热台下降时保持其位置不变。床架是用 ASA 打印的，可以承受 90 摄氏度而不会有问题。推杆机构和加热台下降系统由步进电机驱动，步进电机连接到打印机控制板上的备用电机输出。问题中的打印机是 Voron 2.4，由于其高打印速度，非常适合这种应用。

这个工具更换系统只是第一个原型，但它仍然工作得很好。[Thomas]计划进行关键改进，如加大打印床和降低高度。这个系统可能很适合小型和大型印刷农场。我们已经看到了另一个[床清理系统](https://hackaday.com/2020/07/20/automated-part-removal-gets-serious-with-the-chain-production-add-on/)，它不需要额外的构建表面，而是刮去完成的部分。

 [https://www.youtube.com/embed/8O9E9rcH6Us?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=102&wmode=transparent](https://www.youtube.com/embed/8O9E9rcH6Us?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=102&wmode=transparent)

