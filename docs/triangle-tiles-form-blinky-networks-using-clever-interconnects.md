# 三角形瓦片利用巧妙的互连形成闪亮的网络

> 原文：<https://hackaday.com/2021/06/07/triangle-tiles-form-blinky-networks-using-clever-interconnects/>

我们喜欢看到各种形状和大小的 led 灯组合在一起，所以当我们看到[Debra Ansell]的(也称为[GeekMomProjects]) [联锁三角形光面板系统](https://github.com/geekmomprojects/TriangleLightPanel)在我们的屏幕上发光时，我们特别兴奋。这个形状不同寻常的阵列看起来能够自我支撑，并且发出明亮的光，所以我们必须了解更多。![](img/3503dedd6ac7e2e3c5787c72e58392eb.png)

TriangleLightPanel 是一个单一的、三角形的灯光面板(当所有的东西都在名字里的时候会让人耳目一新，不是吗？).每个面板由一个白色 PCBA 组成，上面有三个向内的侧面发光的 SK6812 LEDs，覆盖着透明的丙烯酸树脂。当 led 发挥作用时，三位置排列和反射 PCB 表面确实能充分漫射光线，非常有效地照亮每块玻璃(如果不是完全均匀的话)。鉴于其简单的结构，很难想象如何对其进行重大改进。

真正的诀窍是机械装置。[Debra]没有使用传统的杜邦跳线和 0.1”接头或某种边缘连接器，而是使用了弹簧触点。但是如果你对缺少边缘电镀的手指感到困惑，请三思；连接器是背面简单的电镀条。还有第二个 PCBA，它有效地充当导线和安装弹簧触点的表面，用螺栓固定在连接叶片的背面，以桥接每个节点。在任何情况下，瓷砖都需要机械连接，因此这是一种将电气连接与必要的机械连接相结合的非常简单的方法。

所有必需的源文件都可以在[项目的 GitHub 页面](https://github.com/geekmomprojects/TriangleLightPanel)上找到，宣布该项目的原始推文[在这里供参考](https://twitter.com/GeekMomProjects/status/1270077982439124993?s=19)。我们迫不及待地想看看再增加 30 或 40 个节点会是什么样子！有事业心的黑客已经在建立他们自己的系统；见[【Arturo 182】休息后 24 瓦阵发光](https://twitter.com/arturo182/status/1396133968488054789)。

> 不幸的是，我用完了螺丝和螺母，每片叶子需要 4 个，它们比我预期的要快。尽快订购更多😅
> 
> 不管怎样，我的叶子正在生长:)🌿
> 
> (由 RP2040 邮票+载体提供动力)[pic.twitter.com/rOWOojFnDa](https://t.co/rOWOojFnDa)
> 
> —Arturo 182(@ Arturo 182)[2021 年 5 月 22 日](https://twitter.com/arturo182/status/1396133968488054789?ref_src=twsrc%5Etfw)