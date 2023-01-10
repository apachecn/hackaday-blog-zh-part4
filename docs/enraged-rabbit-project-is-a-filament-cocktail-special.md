# 愤怒的兔子项目是一个灯丝鸡尾酒特别

> 原文：<https://hackaday.com/2021/10/04/enraged-rabbit-project-is-a-filament-cocktail-special/>

自从 3D 打印机出现以来，似乎我们许多人都梦想着多色 3D 打印的喷嘴共享解决方案。仅仅因为 Prusa 的 MMU 成为焦点已经有一段时间了，并不意味着没有空间去设计一些原创的东西。如果你渴望一些新的东西来让你大饱眼福，看看[EtteGit]的 [EnragedRabbitProject](https://github.com/EtteGit/EnragedRabbitProject) 就知道了。专为 Voron 3D 打印机打造，这是一款可扩展的灯丝更换解决方案，从头开始设计，可扩展至容纳多达 9 根灯丝。

EnragedRabbitProject 分为四个主要部分。首先是愤怒的兔子*胡萝卜喂料器* (ERCF)，这个系统处理细丝的选择、收回和装载。接下来，是*胡萝卜补丁* (ERCP)，每个线轴都需要一个线轴固定器/缓冲器组合。对于那些不熟悉换丝器的人来说，解开灯丝很容易，但是把它重新绕回线轴就很难了。由于喷嘴在切换长丝时会收回相当长的长丝，因此控制所有这些额外松散的长丝以防止缠结是很重要的。细丝缓冲液是解决方案；这是对线轴支架的一个巧妙的机械添加，将管理在这些灯丝更换期间松开的额外灯丝。在这两个系统之外是*王座* (ERKS)一个 Voron-2 设置，它将多余的灯丝清洗成珠子而不是清洗块，最后是*灯丝传感器*，它检测灯丝变化的灯丝存在。

有时很难理解这类数控系统的可靠性。在这一点上，请记住，该项目的登录页面上的打印是数百甚至数千根灯丝交换的结果——这确实是一个惊人的壮举。超越可靠性的是项目的呈现。[EtteGit]已经友好地发布了所有机械组件的 STEP 和 STL 文件，Klipper 配置文件，以及一个[物料清单](https://docs.google.com/spreadsheets/d/1A_qeNeaVprh_iPbvLcLjvJ2o2NfCzjuJam3K3RkWW0w)，它将根据您正在安装的灯丝数量进行缩放。

我们很高兴看到人们继续创新多色或多材料 3D 打印机的概念。对于其他多丝设置，请查看[Paul Paukstelis'] [显微镜启发的头部更换器](https://hackaday.com/2019/05/15/microscope-inspired-toolchanger-spins-multicolor-3d-prints/)和[MihaiDesigns'] [可拆卸工具头概念](https://hackaday.com/2021/04/13/removable-extruder-pulls-out-the-stops-on-features/)。

[https://streamable.com/o/3lo192#?secret=OTRgksLdMA](https://streamable.com/o/3lo192#?secret=OTRgksLdMA)