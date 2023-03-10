# 为 KiCad PCBs 设计 3D 印刷外壳

> 原文：<https://hackaday.com/2020/07/07/designing-3d-printed-enclosures-for-kicad-pcbs/>

如果您以前使用过 KiCad，您肯定会对方便的 3D 视图很熟悉，该视图向您显示了组装好的电路板的渲染视图。但是正如[Vadim Panov]所解释的，你可以将这种能力更进一步。通过一些额外的工具和一点点专业知识，[您可以利用 KiCad 的 PCB 渲染来定制 3D 可打印外壳](https://www.shortn0tes.com/2020/04/modeling-ready-pcbs-in-kicad-for-enclosures.html)。

第一步是像通常在 KiCad 中那样设计 PCB。这可能是您自己发明的原始 PCB，或者是您想要为其构建外壳的现成模型的数字表示。如果是后者，那么 PCB 不需要 100%精确；我们的目标实际上只是将大部件放入大致正确的区域，这样就可以获得正确的间隙。虽然很明显，你要确保电路板的外部尺寸和安装孔的位置尽可能准确地重新创建。

[![](img/83b26f7bb58ef93adafa2a80c60120de.png)](https://hackaday.com/wp-content/uploads/2020/06/kicad3d_detail.png) 从那里，[【Vadim】推荐了一个叫升压](https://kicad.org/external-tools/stepup/)的工具。这将获取您的 PCB KiCad PCB 文件，并创建组装电路板的 STEP 或 STL 文件，该文件可导入到您选择的 Cad 软件包中。为了这个演示的目的，他坚持使用 FreeCAD，因为他喜欢它从头到尾都是一个完全自由/开源软件工具链的想法。

现在你的 CAD 软件中已经有了 PCB 的模型，剩下的就看你的了。当然，您可以使用现有的外壳型号，例如我们之前介绍过的“终极盒子制造商”[生产的型号，但是您也可以轻松地开始围绕数字 PCB 构建新的外壳。](https://hackaday.com/2018/03/02/printed-it-custom-enclosure-generator/)

寻找更多的指导？碰巧的是，作为我们最近发起的 [HackadayU 计划](https://hackaday.com/2020/06/17/schools-in-session-with-hackadayu/)的一部分，我们自己的【Anool Mahidharia】将[介绍如何开发 KiCad + FreeCAD 工作流](https://www.eventbrite.com/e/hackadayu-kicad-freecad-tickets-109682641734)。