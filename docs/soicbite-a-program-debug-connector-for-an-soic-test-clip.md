# SOICbite:用于 SOIC 测试夹的编程/调试连接器

> 原文：<https://hackaday.com/2019/06/13/soicbite-a-program-debug-connector-for-an-soic-test-clip/>

这个问题是众所周知的:编程和调试头消耗了宝贵的电路板空间，而连接器要花钱。尤其麻烦的是无处不在的 100 密耳引脚接头，不是因为它们很贵，而是因为它们很大，尤其是沿 z 轴方向。如果你在建造微型设备，这些东西会占据很大的空间。通过一些巧妙的思考，[Simon Merrett]找到了一种方法来重复使用我们许多人已经拥有的东西——SOIC-8 测试夹——[连接到 PCB 上的一个特殊足迹，而不需要另一个连接器](https://hackaday.io/project/165917-soicbite-programmingdebug-connector-footprint)。他称这个系统为 SOICbite。

SOIC 夹附着在一个由八个焊盘(PCB 每侧四个)和五个非电镀通孔组成的封装上，用于固定夹。将 PCB 尺寸与可拆卸连接器直接匹配的想法并不全新——Tag Connect 已经这样做了一段时间，但连接器价格昂贵且来源单一。另一方面，不同质量的 SOIC 测试剪辑可以从许多供应商那里买到，包括在你最喜欢的网站上非常便宜的交易。我们可以看到的一个缺点是，SOICbite 引脚必须位于 PCB 边缘，才能与夹片正确匹配。然而，空间和成本的节省可以很好地弥补这一点。

[Simon]已经在 GitHub repo 中提供了他的 KiCAD 足迹，并且也提供了任何其他 CAD 包的足迹。所以，发动你喜欢的工具，为他画一个，让这些东西被广泛采用，因为我们认为这是一个伟大的想法。

对于商业选择，请查看我们在 2014 年对 Tag Connect 的[报道。](https://hackaday.com/2014/04/27/a-small-replacement-for-large-programming-headers/)