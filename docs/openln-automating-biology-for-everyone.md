# OpenLH:为每个人自动化生物学

> 原文：<https://hackaday.com/2018/12/16/openln-automating-biology-for-everyone/>

当我们在生物实验室的时候，你必须用吸管来转移液体。用嘴叼起危险的东西似乎总是很奇怪。效率也不是很高。现代实验室将使用液体处理机器人，但这些并不便宜。有时这些被称为移液器，即使是易贝上的二手移液器平均也要花费你 1000 美元——其中许多远不止这个数。现在有了一个开源的替代物，OpenLH，它可以以不到 1000 美元的价格构建，利用开源的机器人手臂。你可以在下面找到一个关于这个系统的视频。

机器人手臂，一个 uArm Swift Pro，是成本的大头。只要稍加努力，Pro 还可以作为 3D 打印机或激光雕刻机进行操作。事实上，我们想知道你是否可以使用手臂制造 3D 打印机，然后打印你需要的部件，将其转换为液体处理器。看起来应该有用。

3D 打印的零件支撑着移液器和注射器组件。如你所料，还有额外的马达来操作活塞。

对于编程，该设备使用 Python 和 Blockly——如果您不想编写实际代码，可以使用后者。有一个生物打印应用的例子，帖子声称精度在 0.15 微升以内。

很自然的，我们想到了用它来做[焊膏](https://hackaday.com/2014/04/02/dispensing-solder-paste-with-a-3d-printer/)。这真的让我们想起了过去见过的许多[漫画家](https://hackaday.com/2013/10/16/3d-printering-pastestruders/)，但是非常精确。

 [https://www.youtube.com/embed/r-m2pXBq76A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/r-m2pXBq76A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

