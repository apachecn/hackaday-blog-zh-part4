# 为您的下一个 OpenSCAD 项目尝试 NopSCADlib

> 原文：<https://hackaday.com/2019/06/15/try-nopscadlib-for-your-next-openscad-project/>

本网站的大多数读者现在都熟悉 OpenSCAD 3D 建模软件，您可以在其中编写代码来创建 3D 模型。你可能已经使用 OpenSCAD 为你的 3D 打印机输出了一些 STL 文件。但多年来，[nophead]一直在推动 OpenSCAD 的发展，创建了一些复杂的实用程序和零件库来帮助建模，以及一套 Python 脚本来生成可打印的 STL、激光就绪的 DXF、物料清单和人类可读的装配指令，以及分解视图子装配的 PNG 图像。

最近[nophead]整理了所有这些 OpenSCAD 基础设施，并在 GitHub 上发布为 NopSCADlib。您可以通过浏览存储库中的示例项目和自述文件，以及阅读 HydraRaptor 博客上的[公告博客来了解更多信息。一些功能亮点包括:](https://hydraraptor.blogspot.com/2019/06/nopscadlib.html)

*   一个大型零件库，里面装满了马达、按钮、光杆等等
*   许多实用功能有助于倒角、圆角、精密孔、子组件和 BOM 生成
*   Python 脚本自动输出 STL、DXF 和 BOM
*   从嵌入在 OpenSCAD 文件中的 Markdown 自动创建文档
*   分解子组件的自动渲染

所缺少的是一个很好的 Makefile 来把它们联系在一起！如果你像我们一样，一想到在将 3D 项目“编译”到现实世界之前将它们放入版本控制中就头晕目眩，那就在你的下一个项目中尝试一下吧。

我们之前讨论过一些复杂的 OpenSCAD:[掌握 OpenSCAD 工作流程](https://hackaday.com/2018/11/14/mastering-openscad-workflow/)，以及[一个 OpenSCAD 迷你 ITX 电脑机箱](https://hackaday.com/2018/11/05/an-openscad-mini-itx-computer-case/)。