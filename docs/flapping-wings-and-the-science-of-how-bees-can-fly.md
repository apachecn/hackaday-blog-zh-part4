# 拍打翅膀和蜜蜂如何飞行的科学

> 原文：<https://hackaday.com/2021/02/22/flapping-wings-and-the-science-of-how-bees-can-fly/>

杰瑞·宋飞以《蜜蜂电影》开始了他的职业生涯，这是一部以昆虫为主题的动画电影，在 2007 年风靡全球。这提出了一个难题——根据所有已知的航空法则，蜜蜂应该不会飞。尽管如此，蜜蜂还是会飞，因为蜜蜂不会在乎人类认为不可能的事情。

这句话不容易被特别归因于任何人，但它是一个关于在工程背景下做出错误假设的警示故事。是的，如果你用和客机一样的数学方法给蜜蜂建模，你当然会发现它不应该会飞。它的小翅膀不可能产生足够的升力使它的身体离开地面。但那是因为这个假设是错误的——因为蜜蜂不像飞机那样飞行。蜜蜂拍动翅膀。但这只是开始。事实是更加复杂和有趣的！

## 扑翼和动态失速

![](img/35e20bc695b90b5d6c81e1e5d6330115.png)

Smoke visualization of a hawk moth. Peeling apart the mysteries of flapping wing flight has required intensely difficult work to visualise complex three-dimensional flow regimes around tiny, uncooperative insects. ([(Willmott, Ellington & Thomas, 1997)](https://www.researchgate.net/figure/The-leading-edge-vortex-increases-in-size-with-forward-speed-For-smoke-at-the-same_fig4_25456631)

普通飞机有固定的机翼，实际上相对来说是刚性的。有一些结构的灵活性，但从空气动力学的角度来看，它没有明显的影响。由于它们的翼型形状，这些翅膀在空中高速移动时会产生升力。增加机翼相对于气流的角度，例如，通过上仰飞机，机翼将产生更大的升力。这个角度叫做 *[攻角](https://en.wikipedia.org/wiki/Angle_of_attack)。*增加得太多，气流会与机翼分离，从而完全停止产生升力。这叫做*地摊*。没有升力，飞机就会从空中掉下来。

像鸟类和许多昆虫一样，蜜蜂没有固定的翅膀——相反，它们拍打翅膀来产生推进力和升力。翅膀以令人难以置信的复杂动作扇动，在下行和上行过程中，翅膀一直旋转，以实现效率最大化。用扑翼[创造高升力的关键在于各种复杂的流体机制](https://jeb.biologists.org/content/jexbio/219/7/920.full.pdf)。

![](img/110fb1761fe36140e4a6e8ffa7e6915d.png)

The leading edge vortex, as visualised on a model of a hovering hawkmoth. Note how the leading edge vortex stays attached to the wing on the downstroke from (a) to (b). ([van den Berg, Ellington 1997](https://www.researchgate.net/figure/Flow-visualization-of-the-leading-edge-vortex-during-the-downstroke-Smoke-was-released_fig10_285599012))

第一种是通过称为*动态失速、*或*无失速*的现象产生强前缘涡流。这是机翼在下行和上行时处于令人难以置信的高攻角的地方，这导致机翼上的气流分离，产生一个附着在机翼前缘的大旋涡。由于沿着机翼翼展产生的流动特征，这个涡流仍然附着在机翼上，这与三角翼在飞机上的工作方式非常相似。通过保持这种旋涡附着，机翼能够产生高升力，这是由于机翼上的压力差，如果允许旋涡消散，这种压力差将会消失。

第二是旋转效应。可以在改变冲程方向之前、改变冲程方向期间或改变冲程方向之后旋转机翼。当机翼旋转时，这种运动增加了机翼周围现有涡流的环流。在改变行程之前这样做，空气中增加的循环会增加机翼产生的升力；之后这样做会产生一个负升力。对称地做这件事会在整个翼拍过程中产生正负升力峰值。通过改变旋转点，就有可能改变机翼每一次拍打产生的升力。

![](img/f2e722b6126ef6ef8e6865f1dd66fd19.png)

A diagram showing the difference in aerodynamic performance of wings during advanced, symmetrical, and delayed rotation regimes. The black lines represent the wing, with the dot showing the leading edge. The red arrows show the magnitude and direction of the instantaneous forces on the wing. This data was collected with a robotic flapping wing model. [(Dickinson, Lehmann & Sane, 1999)](https://www.researchgate.net/publication/12926194_Wing_Rotation_and_the_Aerodynamic_Basis_of_Insect_Flight)

在各种类型的昆虫和鸟类中也观察到了其他复杂的机制，许多物种表现出独特而多样的拍打技术。在蝴蝶身上观察到的一种技术是机翼-尾流的相互作用。尾流是在运动物体后面的流体中看到的流动状态；最常被人类观察到的是船在水中行驶时水流的变化。这也适用于空气中的翅膀。在机翼-尾流相互作用中，机翼在拍动过程中的运动在机翼气流和前一次拍动产生的尾流之间产生相互作用。由于空气中的尾流由拍动的翅膀引起的流体运动组成，与这种尾流相互作用以产生更多升力使得昆虫能够重新获得一些已经消耗的能量以提高其效率。

另一个被普遍引用的机制是“拍打和投掷”，即昆虫两侧的翅膀在上行冲程的顶部被拍在一起，挤出它们之间的空气，帮助产生推力，然后分开开始下行冲程。当翅膀剥离时，它们在它们之间产生了一个低压区，吸入空气，有助于在下行时建立循环。然而，这种方法不是所有物种都使用的，只在某些飞行状态下使用，所以不是常规扑翼飞行的关键组成部分。

总的来说，扑翼飞行背后的流体力学非常复杂。即使是解析这个非常简单的解释器也需要对流体力学有一个基本的理解，更不用说真正深入主题了。扑翼飞行仍然没有被完全理解，并且是全世界正在进行的研究领域。原因之一是研究这些现象的难度很高。

特别是对于昆虫的飞行，流动状态是微小的，难以观察。这导致了诸如[建造更大规模的昆虫翅膀系统的机器人模拟物](https://www.researchgate.net/publication/12926194_Wing_Rotation_and_the_Aerodynamic_Basis_of_Insect_Flight)和移动翅膀表面通过矿物油罐以更好地看到和理解起作用的机制的技术。[这使得染料可视化等技术得以使用](https://www.youtube.com/watch?v=TmE0qUmnpoU&has_verified=1)，从而深入了解复杂的三维流态。其他工作包括研究更大更容易观察的鸟类，以及运行计算机模型。然而，要证实任何理论，总是需要直接研究实物。

不管有多复杂，古老的格言“蜜蜂不会飞”被证明是错误的，并且更多的是源于做出不恰当的工程假设，而不是任何主要的物理悖论。和往常一样，在运行模拟时，确保一开始就建模正确的东西是值得的。