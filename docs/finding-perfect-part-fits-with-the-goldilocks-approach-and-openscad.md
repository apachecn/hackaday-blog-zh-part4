# 用 Goldilocks 方法(和 OpenSCAD)找到完美的零件

> 原文：<https://hackaday.com/2020/06/09/finding-perfect-part-fits-with-the-goldilocks-approach-and-openscad/>

蛮力或试错法解决问题是有道理的，尤其是当找到一个有经验成分的解决方案时。[Tommy]意识到，当需要设计和 3D 打印尽可能适合工厂伺服系统的伺服喇叭时，情况就是如此，[使用 OpenSCAD 打印“金发姑娘阵列”,通过使试错过程更加高效，可以从中找到与他的打印机完全匹配的产品](https://blog.tommy.sh/posts/quick-tip-hone-in-on-the-perfect-fit-with-a-goldilocks-array/)。通过打印一个零件，[汤米]可以试装几十个选项。

[![](img/7907dbab43457bba4a6debaa196586d3.png)](https://hackaday.com/wp-content/uploads/2020/06/Goldilocks-Array.png) 之所以有必要这样做，是因为每台 3D 打印机在复制小特征和尺寸的精确度方面都有一些差异。例如，CAD 模型中直径为 6.3 毫米的孔在 3D 打印的物体中不会精确到 6.3 毫米。它会偏离一些量，但通常是持续的。因此，解决这个问题的一种方法是根据经验确定哪些测量结果最合适，并在特定的 3D 打印机上使用这些测量结果。

这正是[Tommy]所做的，使用 OpenSCAD 生成大小和形状略有不同的数组。阵列被打印出来，伺服系统被测试，无论哪个选项最合适，都有其用于生产的尺寸。这个概念可以用多种方式实现，由于其编程性质，OpenSCAD 是一个不错的选择。对 OpenSCAD 感兴趣？它可以在几乎任何硬件上运行，并且[你可以在大约不到十分钟的时间内完成基本操作](https://hackaday.com/2013/12/11/3d-printering-making-a-thing-with-openscad/)。