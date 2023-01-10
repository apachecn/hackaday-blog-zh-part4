# 新发布的 FidoCadJ 到处绘制示意图

> 原文：<https://hackaday.com/2020/07/26/new-release-of-fidocadj-draws-schematics-everywhere/>

你还记得画你的第一个原理图吗？想必你用了一支钢笔或铅笔和某种纸。然而，原理图捕获软件使绘制原理图变得更加容易。有很多可供选择的，但我们花了一些时间检查了一下 [FidoCadJ](http://darwinne.github.io/FidoCadJ/index.html) ，发现它很有能力。当然，还有许多其他选择，但我们确实喜欢 FidoCadJ 在本地运行，因为它使用 Java，所以可以在任何计算机上运行。因为它是[开源的](https://github.com/DarwinNE/FidoCadJ)，你可以修改它，你不必担心为你的许多计算机或你的团队授权。

该程序是一个 JAR 文件，我们第一次尝试运行它时，与默认 Java 运行时环境的旧版本发生了冲突。但是这很容易解决，特别是因为有一个更新的版本，只是不是默认版本。

Java 和 PC 已经有了很大的发展，所以这个程序在现代计算机上很快，反应也很快。有一个非常好的元件库和 PCB 封装库，还有其他可用的库，因此您可以使用该工具实际布局一个 PC 板，尽管我们不建议这样做。

该程序可以导出为多种格式，尽管我们希望与其他程序有更多的互操作性。它确实创建了 Eagle 脚本和 gEDA。pcb 格式文件。例如，我们看不到一种简单的方法来将它们导入 KiCAD，或者甚至为普通的自动程序生成文件。然而，这也不是该项目的真正目标。根据他们的常见问题:

> 我已经在用 Kicad，LTSpice，Cadence，Mentor，Altium 或者 Visio，为什么 FidoCadJ 有意思？
> 
> 因为它是追求不同目的的不同程序。它是大型 EDA 电子工具的补充。有没有尝试过在文档或演示文稿中包含您的原理图？你对结果满意吗？
> 
> 如果您想发布和共享您的绘图，但对网表功能和仿真不感兴趣，FidoCadJ 可能是您的理想工具。它是 LaTeX 友好的:您可以导出 PGF/TikZ 脚本中的绘图，并将其包含在您的文档中。

当然，这个程序和 KiCAD 都使用 ASCII 文件，代码是可见的，所以如果你写了一个转换器，让我们知道。

当然，[创建原理图](https://hackaday.com/2019/03/19/ask-hackaday-how-do-you-draw-schematics/)的方法有很多种。如果你不介意[云](https://hackaday.com/2017/12/05/easyeda-two-years-later/)就更是如此。