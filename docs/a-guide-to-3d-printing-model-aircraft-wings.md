# 3D 打印飞机机翼模型指南

> 原文：<https://hackaday.com/2022/08/26/a-guide-to-3d-printing-model-aircraft-wings/>

机翼的确切翼型形状对飞机的性能和效率有很大的影响，将根据预定的飞行包线进行选择。如果你正在超越泡沫板机翼，3D 打印是一种创建精确机翼的绝佳方式，而[汤姆·斯坦顿]为我们提供了一个很好的指南，让我们能够[建模机翼部分，从而轻松打印](https://www.youtube.com/watch?v=QJjhMan6T_E)。

[Tom]在休息后使用视频中演示的过程为他最新的[垂直起降遥控飞机](https://hackaday.com/2022/08/22/optimising-a-rc-tilt-rotor-vtol/)制作机翼。上面印着[轻质 PLA](https://hackaday.com/2020/02/17/bubbly-filament-works-better-than-you-think/) ，停止挤压会渗出很厉害。为了解决这个问题，他设计了翅膀和它们的内部肋，在一条连续挤压线上印刷。

他想要一个能够从悬停平稳过渡到向前飞行的机翼，并使用[翼型工具网站](http://airfoiltools.com/)找到并下载合适的翼型。将轮廓导入 Fusion 360 后，他以对角线网格模式创建了内部肋，沿机翼长度方向有减轻孔。一个圆柱体沿着机翼的核心延伸，以安装碳纤维翼梁。在 CAD 中，肋骨首先被视为一个独立的实体，并被分割成四个象限。当这些象限与外壳结合时，它允许切片机使用“[花瓶模式](https://hackaday.com/2022/05/15/3d-printing-hack-leverages-vase-mode-structurally/)”将整个印刷品视为连续的外部周边线。

这些步骤看起来很简单，但是花了大约 3 周的实验才找到一个可行的过程。它主要是为具有连续外形的直机翼设计的，但也应该适用于锥形/后掠机翼。当把飞机推向效率的边缘时，一个设计良好的机身是必不可少的，就像太阳能飞机能在夜间飞行一样。

 [https://www.youtube.com/embed/QJjhMan6T_E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QJjhMan6T_E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

