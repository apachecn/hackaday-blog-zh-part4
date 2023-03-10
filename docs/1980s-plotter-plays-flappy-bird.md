# 80 年代绘图仪播放 Flappy Bird

> 原文：<https://hackaday.com/2019/06/08/1980s-plotter-plays-flappy-bird/>

如果你碰巧有一台 HP7440A 或类似的绘图仪，你可以玩一个快速的 Flappy Bird 游戏——或者[卫斯理公会]称之为[Plotty Bird](https://github.com/WesleyAC/plotty-bird)。只要确保你有一些空白纸。根据作者的说法，整个过程可以容纳大约 200 行 Rust 代码，每秒大约 20 帧。

看着这个东西走，它似乎随机绘制了一组管道，然后在同一页面上实时跟踪你的飞行路径。

当然，这不是很实际，但是我们喜欢这个想法，看着绘图仪运行仅次于看着 3D 打印机。当然，如果你使用 GCode 重写代码，你可以用一台 3D 打印机和一支安装在上面的笔来做类似的特技。代码足够短，也足够清晰，如果你愿意的话，学习更多关于 Rust 的知识并不是一个坏借口。

如果你想理解代码或修改它，你可能会找到一个 [HPGL 参考](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)得心应手。格式非常简单:两个字符、通常由逗号或回车符分隔的参数以及结束数据包的分号。

如果你没有老式的硬件，你可以[建造自己的](https://hackaday.com/2019/01/30/pen-plotter-from-salvaged-printer-parts/)。如果你不想啃坏打印机，你可以随时拆开一个 [DVD 驱动器](https://hackaday.com/2019/04/29/build-a-plotter-using-scrap-dvd-drives/)。