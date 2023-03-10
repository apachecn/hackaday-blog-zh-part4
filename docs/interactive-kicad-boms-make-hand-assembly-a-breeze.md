# 交互式 KiCAD BOMs 使手工组装变得轻而易举

> 原文：<https://hackaday.com/2018/09/04/interactive-kicad-boms-make-hand-assembly-a-breeze/>

我们都经历过。你终于得到了最后一个 DigiKey 盒子，现在你的桌子上布满了零件，可以塞进你一直在工作的闪亮的新 PCB。第一站？被动镇，人口无尽波 1uF 电容。第一个放在左上角，然后再下面一点，然后…一旦你到了 C157，就很难准确地记住哪个部分放在哪里了。输入字面上的名字 [InteractiveHtmlBom](https://github.com/openscopeproject/InteractiveHtmlBom) (IHB)来平滑这个过程。

IHB 使将 BOM 中的行映射到电路板上的物理位置这一令人沮丧的任务变得简单。传统的方法当然是查看 BOM，然后在电路板上搜索该标志并放置元件。(你在丝绸上留下了标记，对吗？)或查看 BOM，要求您的 CAD 软件包在布局中搜索该零件，然后放置。IHB 自动生成了一个文档。

![](img/7b3d15610e0a2220c9b1e3781bd9868a.png)

A sample file from [a familiar project](https://hackaday.com/2018/08/29/faded-beauty-dmm-gets-an-oled-makeover/)

运行该工具，无论是独立的还是作为 KiCAD 5.0 的插件，您都会得到一个包含新的交互式 BOM 的文件夹。有几个视图选项，但一般来说，它在一个窗格中显示带有指示器和值的 BOM 视图，在另一个窗格中显示电路板的顶部和/或底部。当您将鼠标悬停在 BOM 行上时，它会在纸板视图中突出显示相关零件！有切换过滤顶部和底部的董事会，标记哪些部分已被放置，光和暗模式等。此外，还能够根据指示符和值进行过滤和排序。如果它只是那些光滑的可滚动/可平移面板渲染的生成器/查看器，我们会印象深刻的！

休息后查看一个很长的 GIF 演示，或者在这里探索许多预先创建的演示材料中的一个。我们偏爱 [OSPx201](https://openscopeproject.org/InteractiveHtmlBomDemo/OSPx201/ibom.html) 。

感谢[GregDavill]的提示！

![](img/7f3a9f5fa5a103f53b0b9ea4a3781640.png)