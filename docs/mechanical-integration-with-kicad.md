# 与 KiCad 的机械集成

> 原文：<https://hackaday.com/2019/04/22/mechanical-integration-with-kicad/>

Eagle 和 Fusion 在集成电子和机械设计方面获得了所有的尊重，但 KiCad 呢？有没有什么工具可以让你轻松地为下一个印刷电路板构建外壳？[Maurice]有一个解决方案，[，它无缝同步 KiCad 和 FreeCAD](https://hackaday.io/project/161114-kicad-stepup-a-seamless-ecad-mcad-synchronization) 。KiCad 将为您提供电路板，FreeCAD 将为您提供机箱，这样您就可以完全实现 eCAD 和 MCAD 同步。

这个技巧以 FreeCAD 宏的形式出现(Github 上的[，带有一堆文档)，它将 KiCad 板和组件加载到 FreeCAD 中，并将其导出为 STEP 文件。您可以在 FreeCAD 中对齐 KiCad 板，将步骤转换为 VRMLs，检查干涉和碰撞，并在 KiCad 板周围创建一个外壳。](https://github.com/easyw/kicadStepUpMod)

在过去的几年里，KiCad 已经获得了一些非常棒的可视化工具，如果我们没有提到它是在生产前可视化完整电路板的最佳方式之一，那将是我们的失职。从电子 CAD 到机械 CAD 的飞跃在 KiCad 生态系统中仍然是相对罕见的，并且总是需要更多的工具来实现这一点。