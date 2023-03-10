# 程序生成的树

> 原文：<https://hackaday.com/2020/11/20/procedurally-generated-trees/>

当树叶从北半球这里的树上落下时，迎接我们的是构成树木骨架的树枝和树枝的清晰景象。[Nicolas McDonald]在观察树木时做了一个简单的观察，当树枝分叉时，横截面积的总和是守恒的。这个观察也是达芬奇做的(根据帕米拉·泰勒的《达芬奇笔记》)。受到观察的启发，[Nicolas]决定[为自己的好奇心](https://weigert.vsos.ethz.ch/2020/10/19/transport-oriented-growth-and-procedural-trees/)制作一棵树的模型。

该模拟试图模拟树木如何传播养分。养分从根部流向四肢，按比例分配到各个部位。[Nicolas']模型只允许二分分裂，但有些植物分裂成三种方式，而不是两种方式。在哪里分裂的决定有些武断，因为[Nicolas]还没有找到大自然使用的任何规则或方法。它最终只是一个硬编码的值，乘以基于分支深度的指数衰减。分裂的方向由叶子的密度、分枝的大小和母分枝的方向决定。最重要的是，每一个超过一定深度的分支末端都附着了一个粒子云。

通过调整不同的参数，该模型可以生成不同的物种，如常青树和盆景般的树木。[代码托管在 GitHub](https://github.com/weigert/TinyEngine/tree/master/examples/6_Tree) 上，我们对实际的树模型代码有多小(大约 250 行 C++)印象深刻。进行观察并将其融入到项目中的力量在这里是显而易见的，结果也是非常美好的。如果你正在寻找生活中更程序化的一代，看看这个中世纪城市发电机。