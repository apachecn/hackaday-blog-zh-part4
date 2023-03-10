# 3D 打印黑客从结构上利用花瓶模式

> 原文：<https://hackaday.com/2022/05/15/3d-printing-hack-leverages-vase-mode-structurally/>

从概念上讲，FDM 3D 打印是一个非常简单的过程:你在 3D 空间中定义一组体积，然后切片软件在不断增加的高度上切割模型，计算出内壁和外壁的位置，然后稀疏地填充内部体积，以便将壁连接在一起，并支撑最后添加的顶层。

但是你会很快发现，当模型变得更大更复杂时，打印时间会迅速增加。对于形状简单但结构需求非常低的大型模型来说，一个技巧是使用所谓的“花瓶模式”，以一种细而垂直的螺旋来描绘物体的轮廓。但是这是一个弱的构造方案，并且仅允许有限的建模复杂性。考虑到这一点，这里有[Ben Eadie]的一个[样的中间站技术](https://www.youtube.com/watch?v=STNJbHJf9K0)(视频，嵌入下面)，有些人可能会发现有助于节省打印时间和材料。

![](img/a01dbbb389a1ed59845aca97416e0ab9.png)

This solid shape is mostly cut-through to make supporting ribs between the walls of the shell

这个想法是使用花瓶模式打印，但通过操纵模型的外壳，在周边添加部分贯穿的槽，关键的是，添加一个完全贯穿的槽。

首先，你需要一个模型，它的内壳与外壳的形状相似，你可以挖空一个实体，留下一点厚度。通过使狭槽宽度等于喷嘴尺寸厚度的一半，并使狭槽停止在距外壳相同的距离处，花瓶模式可用于描绘形状的轮廓，在外壳的内壁和外壁之间具有支撑肋。

因为槽比挤出物窄，槽壁将合并成一个实心肋，将物体的壁相互连接，但关键是，仍然允许它在没有任何传统填充物的情况下以连续的螺旋印刷。这是一个有趣的想法，可能有一些优点。

还有其他方法可以让打印的部分变得坚硬，[比如使用表面纹理](https://hackaday.com/2021/04/27/texture-adds-stiffness-to-3d-parts/)，但是如果你对薄壳没意见，但想从中得到一点乐趣，你可以[破解 g 代码，做出一些真正有趣的形状](https://hackaday.com/2022/02/22/bend-your-vase-mode-prints-by-hacking-the-gcode/)。

 [https://www.youtube.com/embed/STNJbHJf9K0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/STNJbHJf9K0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

