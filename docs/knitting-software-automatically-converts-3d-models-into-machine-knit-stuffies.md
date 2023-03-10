# 针织软件自动将 3D 模型转换成机器编织的材料

> 原文：<https://hackaday.com/2019/06/14/knitting-software-automatically-converts-3d-models-into-machine-knit-stuffies/>

在 Hackaday，我们已经看到了很多有趣的编织技巧。在将计算机与针织机相结合的过程中，人们探索了很多创造性的空间，反之亦然，但在很大程度上，最终的针织品都有点……二维。针织和业余爱好者水平的针织机的机械现实只是倾向于在平面上用简单的像素网格工作。

然而，[卡内基梅隆纺织实验室]的一个团队已经将计算机控制的针织世界从二维带到三维，使用[软件可以为你输入的几乎任何 3D 模型创建针织图案](https://textiles-lab.github.io/publications/2018-autoknit/)。你可以把它想象成标准的 3D 打印切片软件，只不过它不是简单的热塑性塑料层，而是用纱线和 100%填充物生成复杂的多维针织链和针织链。

他们在题为 *[的论文中讨论了细节，并很好地说明了 3D 网格的自动机器编织](https://drive.google.com/open?id=1UO0aGgbZqidvzgupqrJ--GwazSmIkph2)* 和一个[视频](https://drive.google.com/file/d/1_XlprMZKhhuk89xsZMMo7Qxv801bRASK/view)(不幸的是不能嵌入)显示了软件界面的运行，以及一些填充过程和最终可爱的(好吧，他们也有点毛骨悚然)填充形状。

自从他们的论文发表以来，[纺织品实验室]也在 GitHub 上发布了他们的 autoknit 软件的开源版本。尽管编译和安装步骤看起来很重要，但实际的界面对于专业爱好者来说似乎很容易理解。任何熟悉 3D slicer 软件的人都应该能够加载一个模型，定义闭合形状所需的两个接缝，填充后需要手动缝合，并输出针织机代码。

以前的编织:[编织宇宙](https://hackaday.com/2018/09/06/electromagnetic-field-a-hacked-knitting-machine-knitting-the-universe/)，[自行车围巾编织者](https://hackaday.com/2018/06/11/bike-driven-scarf-knitter-is-an-accessory-to-warmth/)，[编织电路板](https://hackaday.com/2014/06/19/knitted-circuit-board-lends-flexibility-to-e-textiles/)。