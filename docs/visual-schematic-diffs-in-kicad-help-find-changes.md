# KiCAD 中的可视化示意图差异有助于发现变化

> 原文：<https://hackaday.com/2018/09/19/visual-schematic-diffs-in-kicad-help-find-changes/>

编写软件时，开发工作流程的一个关键部分是查看文件之间的变化。使用版本控制系统，这个过程可以变得非常高级，让您及时看到任意文件和切片之间的变化。工具的存在是为了在 EDA 工具的世界中可视化地做这件事，但是它还没有真正渗透到自由爱好者的层次。但是由于开放和易于理解的文件格式，[jean-nol]已经为 KiCAD 编写了 plotgitsch。

在 EDA 工具的高端领域，如 [OrCAD](https://www.orcad.com/resources/library/orcad-172-2016-capture-design-difference-viewer) 和 [Altium](https://www.altium.com/documentation/18.1/display/ADES/WorkspaceManager_Pnl-Differences((Differences))_AD) ，版本控制系统和设计工具之间有着紧密的集成，VCS 作为一种产品出售，以改善设计工作流程。但是 KiCAD 并没有试图给用户强加一个版本控制系统，所以直接烘焙 VCS 相关的工具并没有什么意义。你*可以*用 git 管理 KiCAD 项目中的变更，但是正如[【jean-nol】指出的那样](https://jnavila.github.io/plotkicadsch/#visual-diffing)阅读 Git 对变更的 X/Y 坐标和库文件路径的文本描述对计算机比对人类更有用。基本上用起来很烂。你真正需要的是一个 diff 工具，它可以向用户显示两个版本之间的变化，而不是描述它。这就是 plotgitsch 所提供的。

plotgitsch 的核心功能是以任意的 Git 版本生成 KiCAD 项目的图像。之后，有两种方法可以查看输出。一个是生成每个版本的图像，这些图像可以输入到一个通用的 visual diff 工具( [UNIX 哲学](https://hackaday.com/2018/09/10/doing-one-thing-well-the-unix-philosophy/)有人知道吗？).文档中有一个示例脚本来帮助进行设置。另一种方法是在 plotgitsch 中生成彩色编码图像，并在用户选择的浏览器中打开它。它可能不会被集成到 EDA 中，但我们会采取一键视觉差异的任何一天！