# 满足您所有 CNC 切割需求的 OpenSCAD 库

> 原文：<https://hackaday.com/2022/01/02/an-openscad-library-for-all-your-cnc-cutting-needs/>

虽然总是存在边缘情况，但如果您使用 OpenSCAD，很有可能您正在处理一个 CAD 模型，您打算在某个时候进行 3D 打印。当然，这并不是说这就是你在 OpenSCAD 中所能做的全部事情，但这无疑是它做得最好的。如果你想制作艺术模型，或者渲染你的新厨房，有其他工具更适合这样的任务。

但是多亏了`lasercut.scad`，一个[库【布兰登·斯莱特】在过去几年里一直在为之工作](https://github.com/bmsleight/lasercut)，我们可能不得不重新考虑我们先入为主的维度概念。他的图书馆不是为 3D 打印设计零件，而是创造用于减法制造的零件。最初(顾名思义),它是面向激光切割的，但该项目已经发展到支持 CNC 路由器，乙烯切割机，以及几乎任何可以遵循 DXF 文件的东西。

[![](img/686689135ead7ef674ed7bf65f22d46f.png)](https://hackaday.com/wp-content/uploads/2021/12/laserscad_detail2.jpg)

This “clip” joint is great for acrylic.

该库具有创建用于从激光切割件构建事物的标准技巧的功能，如指接、系留螺母和装配标签。如果你曾经看到过一个旧的木制 3D 打印机套件，你可能可以用`lasercut.scad`重新创建它。它甚至支持一个相当狂野的旋转细木工，由[马丁·兰斯福德]提供。

没有办法将足够数量的愤怒光子集中到工件上？别担心。此后，该库已被修改为考虑参数锯口宽度，这使您可以在特定工具执行业务时，拨入特定工具将从材料中获取的咬入量。甚至还有处理非常薄的切口的特殊功能，[Brendan]通过用乙烯基薄片组装一个盒子来演示。

当然，那些使用过 OpenSCAD 的人会知道在股票界面的任何地方都没有“导出为 CNC”按钮。因此，为了实际采用您的设计并生成您的裁剪师可以理解的文件，[Brendan]包含了一个 Bash 脚本，它将运行必要的 OpenSCAD 咒语来生成 2D·DXF 文件。

[Brendan]在看到我们最近报道的铝制外壳 OpenSCAD 库后，决定发送这一个。如果你有自己喜欢的项目，可以根据自己的意愿改造一些硬件或软件，[不要不好意思告诉我们](https://hackaday.com/submit-a-tip/)。