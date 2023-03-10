# 3D 打印:Prusa 切片机的过去和未来

> 原文：<https://hackaday.com/2019/05/24/3d-printering-the-past-and-future-of-prusas-slicer/>

如果你拥有一台台式 3D 打印机，你几乎肯定熟悉 Slic3r。即使这个名字听起来并不耳熟，但很有可能你用来将 STLs 转换成你的打印机可以理解的 g 代码的程序正在幕后以某种方式使用 Slic3r。虽然偶尔会有挑战者，但在近十年的大部分时间里，Slic3r 仍然是使用最广泛的开源切片器之一。虽然有些人可能会说，专有切片器在某些方面已经领先，但很难打败免费的。

[![](img/db6d507de961fce4ab57a0c2d6d349d2.png)](https://hackaday.com/wp-content/uploads/2019/05/prusaslicer_logo.png)

因此，当 2016 年 Josef Prusa 宣布他的团队推出 Slic3r 时，这并不令人震惊。该公司希望为他们的 3D 打印机系列提供一款优化的切片机，作为开源的大力支持者，他们将在很大程度上依赖于社区中已经可用的产品是有道理的。其结果是恰如其分地命名为“Slic3r Prusa 版”，或后来被称为 Slic3r PE。

表面上，fork 使 Prusa 能够为他们的特定机器微调打印参数，并实现对产品的支持，如他们的多材料升级，但 Prusa 的开发人员没有花很长时间就开始修复和改进核心 Slic3r 功能。因为这两个项目都是在 GNU Affero 通用公共许可证 v3.0 下发布的，所以所有这些改进都可以移植到最初的 Slic3r 但是这样做将花费相当多的时间和精力，这在社区开发的项目中总是短缺的。

由于 Slic3r PE 仍然生产任何 3D 打印机都可以使用的标准 g 代码，很快人们就开始在非 Prusa 打印机上使用它，因为它有更多的功能。但这只会进一步模糊两个项目之间的界限，尤其是对新用户而言。当出现问题时，可能很难确定谁应该对此负责。与此同时，两个项目之间的差距继续扩大。

随着一个承诺给 Slic3r PE 带来巨大变化的新版本的出现，Josef Prusa 认为事情已经到了一个转折点。在最近的一篇博客文章中，他[宣布从 2.0 版本开始，他们的切片器将从此被称为 PrusaSlicer](https://blog.prusaprinters.org/prusaslicer-2-release/) 。让我们看看这个新的切片器，并找出最终将这两个项目分开的原因。

## 改进的用户体验

就设计而言，Slic3r 的接口，以及 Slic3r PE 的扩展，并不完全是高标准。它当然足够实用，但它的设计从来就不美观。由于 Prusa 的业务是销售相对高端的 3D 打印机，因此不难看出 Slic3r 的斯巴达式外观可能会有点问题。

因此，PrusaSlicer 面向用户的最大变化是一个全新的界面，这一点也不奇怪。对于长期使用 Slic3r 的用户来说，这是很熟悉的，但同时也有更现代的感觉。人们更关注在 3D 预览视图中使用矢量图标执行常见任务，而不是必须深入菜单才能找到它们。侧面板现在有一个选项卡式布局，允许用户根据自己的技能水平选择想要查看的选项数量。总的来说，PrusaSlicer 现在有点让人想起 Ultimaker 的 Cura 切片器；考虑到两家公司都在努力为他们的客户开发易于使用(和支持)的切片机，这似乎是合适的。

[![](img/9c2ab21d439e28b855420a075f7b696a.png)](https://hackaday.com/wp-content/uploads/2019/05/prusaslicer_ss1.png)

对于长期使用 Slic3r PE 的用户来说，他们可能会认为 PrusaSlicer 的新外观只是一层新鲜的油漆，在使用新软件时，你会注意到许多可用性的改进和调整。例如，打印时间和成本的实时估计比以前的版本有了巨大的改进，在以前的版本中，您必须在获得信息之前进行切片和导出。

## 支持的新方法

对于具有复杂几何形状的模型，打印支持结构是一件不可避免的坏事。自动支持生成是每一个切片器的标准特性，但是在一些模型上，它可能会混淆并产生次优的结果。在过去的几年里，Simplify3D 等专有切片器试图通过实现用户可以放置在任何他们想要的地方的定制支持结构来解决这个问题。

伪善者的方法是一种中间立场。支撑仍然是自动生成的，但是用户可以很容易地屏蔽掉不想生成支撑的区域。或者，您可以禁用自动支持生成，除非是在特别指定的区域。

 [![Automatic support](img/9963e7d96e3a7a5ad2a66ec1f5c090c8.png "prusaslicer_support2")](https://hackaday.com/2019/05/24/3d-printering-the-past-and-future-of-prusas-slicer/prusaslicer_support2/) Automatic support [![Enforced support](img/4ef443af7e30b5d16144212691ce7776.png "prusaslicer_support1")](https://hackaday.com/2019/05/24/3d-printering-the-past-and-future-of-prusas-slicer/prusaslicer_support1/) Enforced support

在此示例中，您可以看到自动支撑生成是如何用不必要且难以移除的支撑结构填充零件内部的；浪费塑料并使零件清理变得更加困难。但是通过指定一个应该生成支撑结构的特定区域，可以避免这个问题。

毫无疑问，如果您没有完全了解打印机的优势和劣势，使用该功能很容易给自己带来麻烦。但这通常是这种细粒度控制的代价。

## 光的力量

随着去年 SLA 打印机的发布，Prusa 发现他们需要一个能够支持这种完全不同的 3D 打印技术的切片机。他们决定直接在当时还是 Slic3r PE 的地方实现对基于光的 3D 打印机的支持，而不是创建第二个切片器。因为大部分工作发生在 Slic3r 对等体的 alpha 和 beta 版本中，所以 PrusaSlicer 代表了这种 SLA 功能的大部分第一次出现在稳定版本中。

事实上，Josef Prusa 声称，PrusaSlicer 一经发布，就立即成为最完善和最完整的开源 SLA 切片器。这似乎是一个大胆的主张，但我们不得不承认，我们还没有看到太多进入这个特殊领域的产品与之进行比较。自制 SLA 打印机远不如 FDM 的同类产品普遍，但是随着主要部件成本的下降和[现在在开源工具方面的军备竞赛，也许这种情况很快就会改变。](https://hackaday.com/2016/11/18/3d-printering-smartphone-resin-printers-actually-work/)

## 新的进来，旧的出去

[![](img/cae55effe197f6225aa1c846ad16d175.png)](https://hackaday.com/wp-content/uploads/2017/06/prusacontrolsettings.png)

Simplified settings in PrusaControl

虽然 Slic3r 的核心是用 C++编写的，但包括用户界面在内的高级组件是用 Perl 编写的。根据 Josef Prusa 的说法，多年来，这种组合已被证明是一种挑战。由于很难找到精通该语言的贡献者，以及 wxWidgets 用户界面库的兼容性问题，决定开始用 C++重写这些遗留的 Perl 组件。

总的来说，这种转变是顺利的，但至少有一个功能因为它而被搁置了:USB 打印。如果你更喜欢把你的打印机和电脑连在一起，你现在需要坚持使用 Slic3r PE。目前，PrusaSlicer 只会生成 g 代码。你需要用 [Printrun、【T1 via SD card】、](http://www.pronterface.com/)[之类的东西把它放到你的打印机上，或者有 OctoPrint 设置，这样你就可以通过网络来做](https://hackaday.com/2018/01/03/upgrading-a-3d-printer-with-octoprint/)。

你的 USB 线并不是唯一被放出来的东西。在创建 Slic3r PE 后不久， [Prusa 开始了类似于“B 计划”切片器的工作:PrusaControl](https://hackaday.com/2017/06/12/prusacontrol-the-beginners-slicer/) 。由于认为当前的切片器对初学者来说过于复杂，PrusaControl 被定位为一个最基本的工具，可以让您尽可能少地进行打印。但由于能够根据用户的技能水平调整 PrusaSlicer 的界面，因此决定正式放弃 PrusaControl。

## 展望未来

虽然 PrusaSlicer 有了一个新名字和一长串改进，但它的核心仍然是运行在 Slic3r 上。同样重要的是，它仍然在相同的开源许可下发布。这意味着任何人都可以尝试将这些新特性移植到 vanilla Slic3r 上，如果他们愿意的话。现在，Prusa 的任务是清除 Perl 的代码库，这可能会更加困难，但这肯定不是不可能的。另一方面，Josef Prusa 表示，他的团队完全有意愿合并上游 Slic3r 修复和更改，只要它们对包含在 PrusaSlicer 中有意义。

[![](img/b2b9e620e0ca3f41ef9d3fad29e42917.png)](https://hackaday.com/wp-content/uploads/2016/01/stallman-thumb.jpg)

Stallman Approved

从长远来看，这一举措最终会让 Slic3r 开发人员和 Prusa 的任何人受益。首先，名字的改变应该可以避免他们被不适用于他们代码的错误报告所困扰。随着时间的推移，他们甚至会发现，有了 Prusa 在用户界面方面的领导，他们可以集中精力改进核心切片引擎。

有一件事是肯定的:这就是开源应该如何工作。一个成功的公司接手一个开源项目，将他们自己的资源和人才加入其中，并将其转化为一个新的开源项目，这是一件值得庆祝的事情。我们可以争论名称更改的语义，以及用户群的潜在分裂，但最终代码是存在的，无论谁的名字出现在页面顶部，整个社区都会受益。