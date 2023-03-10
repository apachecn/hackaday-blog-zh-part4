# 如何——以及为什么——避免技术图纸中的公差叠加

> 原文：<https://hackaday.com/2018/07/25/how-and-why-to-avoid-tolerance-stacking-in-your-technical-drawings/>

如果你想制造你的零件设计，你需要给制造商提供一份技术图纸。是的，3D 打印机和许多现代机床依赖于从 3D 模型创建的刀具路径。但是，制造商很有可能会在他们自己的系统中重新创建 3D 模型，而不是使用您提供的系统。或者，他们可能使用传统的手工加工，根本不接触 3D 模型。更重要的是，技术图纸为他们提供了重要信息，告诉他们为了让你接受零件，他们需要多接近你的尺寸。

在技术图纸上，所需的尺寸称为标称尺寸。但是，没有哪种制造是完美的，所以你必须在你接受的东西上留有余地。这个回旋的空间叫做宽容。也许你的零件可能比指定的长一点，但这不会影响功能。也许可以短一点——或者都可以。指定公差是必要的，因为它告诉制造商你给了他们多少回旋余地。

但是，如果不小心的话，公差会带来不可预见的后果。公差提供的回旋余地是绝对必要的，但是如果使用不当，即使制造商严格按照您的说明操作，您也很容易得到无法使用的零件。这通常是因为您将多个公差加在一起，这称为公差叠加。

## 复合问题

![](img/7f077b898d27dc26336816b365f50520.png)

看看上面显示的零件尺寸，你能看出问题吗？乍一看，您可能会断言这告诉制造商最右边的孔可以在距离零件左边缘 189.90 和 190.10 mm 之间。实际上，这实际上告诉他们，它可以是 189.50 到 190.50 毫米之间的任何尺寸。这是因为每个尺寸都是基于它之前的特征，它在两个方向上都有 1/10 毫米的灵活性。这与每个新特性相结合，并且公差叠加，最终会比您预期的波动更大。

现在，完全有可能 1 毫米的总电位变化不会使您的器件无法使用。但是，即使是这样，这仍然是不好的做法，因为不清楚这是否是您的意图。制图规程的全部目的是在传达零件设计时消除模糊性，而公差叠加是非常模糊的。如果你最右边的孔在两个方向都有 0.50 毫米的公差，应该明确说明。

## 使用纵坐标尺寸

如何在不增加公差的情况下明确指定？在本例中，最简单的解决方案是使用坐标标注，所有标注都参考一个实体原点。零件的边是硬边，可能是您想要测量内部特征的位置。因此，可以从左边缘或右边缘使用纵坐标尺寸，如下所示，这样每个孔都有一个非弹性参照，避免公差叠加。

![](img/cfbf722cda59382f1bef7f5c56375ae0.png)

不幸的是，纵坐标尺寸并不适用于所有情况。例如，下面的零件具有放射状排列的特征。尺寸——因此公差——以度为单位，而不是像毫米那样的距离。但是，这仍然是一个公差叠加的情况，第一个和最后一个孔可能会在 132 到 138 度之间的任何地方结束。

![](img/6506550d55d3e435e097b3434ac1dd04.png)

在这种情况下，谨慎的解决方案是将每个维度建立在单个几何参考点的基础上，例如上止点。所以，第二洞是 45 度，第三洞是 90 度，第四洞是 135 度。但是，同样，这只是另一个具体例子的解决方案；你真正需要的是对问题的坚定理解，并运用批判性思维去认识它，并在自己的技术图纸中解决它。

## 不要让他们猜

当从另一个位置可能略有变化的要素测量一个要素的位置时，会发生容差叠加。在某些情况下，你可能希望这样。在上面的例子中，在你的设计中，第三个和第四个孔相隔 45°可能比它们相对于第一个孔或整个零件的位置更重要。你是唯一知道你的零件正常工作需要什么的人，制造商的工作就是尽可能地遵循你的技术图纸。

当你起草技术图纸时，你需要时刻记住这个概念。问问你自己，你愿意给制造商多大的回旋余地。但是，与此同时，问问你自己这个回旋的空间是基于什么。也许某个特定特征需要落在距离零件边缘的特定公差范围内，或者相对于相邻特征精确定位更为重要。只有你知道。

技术图纸的目的是准确地告诉制造商如何制造你的零件，并且做到没有任何潜在的混淆。如果他们严格按照你的图纸，你不能因为他们没有正确猜测你的意图而拒绝交付 1000 个零件。在大多数情况下，机械师不会知道或关心你的设计实际上是如何工作的，他们只关心他们能多精确地坚持你的图纸。所以，完全理解你的图纸在告诉他们什么，以及如何避免像公差叠加这样的问题，这取决于你。