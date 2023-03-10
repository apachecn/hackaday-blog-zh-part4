# 使用标记改善 3D 打印的支持

> 原文：<https://hackaday.com/2020/05/27/improving-3d-printed-supports-with-a-marker/>

任何使用过桌面 3D 打印机的人都熟悉支架的概念。如果您正在处理一个具有悬垂特征的复杂模型，通常需要在其周围打印一个支持材料的“脚手架”。不幸的是，移除支撑物是一件痛苦的事情，并且常常会在完成的印刷品上留下需要处理的痕迹。

为了改善这种情况， [[Tumblebeer]对传统方法](https://forum.prusaprinters.org/forum/english-forum-general-discussion-announcements-and-releases/new-method-of-printing-perfect-supports/)进行了非常独特的修改，我们认为这肯定值得进一步研究。它没有移除*需要*做支撑的材料，但是它确实让移除变得容易多了。这种方法便宜，实施起来相对简单，并且不需要多台挤出机或者像水溶性支持物那样的细丝转换。

[![](img/474d2dc7612cf37b15b81d2b36d66793.png)](https://hackaday.com/wp-content/uploads/2020/05/markersupport_detail1.jpg) 诀窍是在支撑物的顶部和印刷物实际接触的区域之间使用永久性标记作为脱模剂。标记涂层防止两个表面融合，同时仍然提供必要的物理支撑以防止模型下垂或塌陷。

为了测试这一概念，[Tumblebeer]为 Prusa i3 MK3S 配备了一个螺线管驱动的标记支架，该支架悬挂在挤出机组件的侧面。[线圈由运行 OctoPrint](https://hackaday.com/2018/01/03/upgrading-a-3d-printer-with-octoprint/) 的 Raspberry Pi 的 GPIO 引脚驱动，并通过 g 代码文件中的自定义命令接合。它在正常打印过程中保持标记不碍事，并在放下界面涂层时降低标记。

[Tumblebeer]表示，这种方法仍然需要一些手工编码，一些自动化的 g 代码脚本或定制的切片器插件可以大大简化这个过程。我们非常有兴趣看到这个概念的进一步社区发展，因为它似乎有相当大的希望。在挤压机的侧面绑上一个标记可能看起来很复杂，但是与快速切换细丝相比根本不算什么。

 [https://www.youtube.com/embed/oBGl4i668Tg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oBGl4i668Tg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

