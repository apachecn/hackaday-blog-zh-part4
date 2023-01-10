# 六角镜阵列隐藏隐藏信息

> 原文：<https://hackaday.com/2021/11/14/hexagonal-mirror-array-hides-hidden-message/>

[Ben Bartlett]最近订婚了，这个提议有一个独特的帮助，就是 3D 打印的六边形镜子阵列，镜子的角度恰到好处，可以用反射光拼出一条信息。上面显示了一个小测试，投射出一颗心，但真正的测试是一个更大的版本，反映了“嫁给我吧？”日落时变成沙子。谁会拒绝这样的事情呢？对我们所有人来说幸运的是，[Ben]分享了设计和建造这样一个有思想和迷人的设备的所有细节。

![](img/f73f840ee2259525f1c1e48e71a3f9d7.png)

Mirrors on the 3D-printed array are angled just right to reflect light into a message.

本质上，镜子阵列的工作有点像投影仪。每个单独的反射可以被认为是一个像素，每个反射的投影位置可以通过每个镜子的精确角度来修改。在一些 Python 代码的帮助下，[本]计算出了拼出“嫁给我？”所需的精确角度并生成了必要的 3D 模型。一个小规模的测试(如上图所示)取得了成功，之后只需要打印阵列和粘贴一些镜子。

当然，那是简短的版本。在实践中，有相当多的棘手问题证明了使用早期测试来发现隐藏问题的价值。首先，镜子的角度和排列是至关重要的，这意味着任何可能影响阵列形状的东西都是一个潜在的问题。胶水在干燥或固化时会膨胀或改变形状，这可能会稍微改变镜子的角度，所以氰基丙烯酸酯(CA)胶水是首选。然而，一点点的 CA 胶会很快弄脏镜子的表面，所以组装时需要小心。

![](img/7817ce9260cf3857dbfc347dd19b4ec4.png)

The gleaming hexagonal mirrors are reminiscent of the [James Webb Space Telescope](https://hackaday.com/2021/11/02/30-days-of-terror-the-logistics-of-launching-the-james-webb-space-telescope/).

另一个问题是当[Ben]突然意识到，在打印最终装配的 20 个小时后，信息需要被颠倒！按照设计，他打印的阵列会投射“？EM YRRAM“这在测试中没有被发现，因为测试图案(心形)是对称的。幸运的是，我们有时间纠正错误，重新开始，但这是势均力敌。[Ben]的代码有一个可选的可视化功能，这对于验证事情是否真的如预期的那样发展是非常宝贵的。碰巧的是，这个项目直到最后一分钟才完成，在这个重要时刻之前没有足够的时间来 100%检查所有的东西，但结果一切都很好。没有一点神秘和危险的生活算什么？

图片很棒，但你不会后悔花时间通读项目页面(不要错过[带注释的 Python 代码](https://github.com/bencbartlett/3D-printed-mirror-array/blob/main/mirror_array.ipynb))，因为【Ben】进入了正确的细节层次。最终的结果看起来棒极了，是一个迷人故事的绝佳纪念品。