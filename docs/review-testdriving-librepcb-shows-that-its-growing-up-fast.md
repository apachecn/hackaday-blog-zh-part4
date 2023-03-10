# 点评:试驾 LibrePCB 显示其成长迅速

> 原文：<https://hackaday.com/2020/01/22/review-testdriving-librepcb-shows-that-its-growing-up-fast/>

从入门级到数千美元的工作站软件，电子设计人员可以使用大量的 PCB CAD 工具。这是一个大多数玩家都是商业玩家的领域，对于开源爱好者来说，传统上只有两种选择。KiCad 和 gEDA 都是有着大量忠实粉丝的古老套装，但是公平地说，它们都为新手提供了一个陡峭的学习曲线。然而，开源 PCB CAD 领域还有另一个竞争者，那就是崭露头角的 LibrePCB。

这个 GPL 许可的包只开发了几年。LibrePCB 在一年多以前发布了它的第一个正式版本，现在版本为 0.1.3，包含了 GNU/Linux、Windows、MacOS 和 FreeBSD 的构建版本。是时候下载并测试它了，看看它是否准备好了。

## 了解图书馆

[![The schematic editor in action, with my simple op-amp mixer as a test project.](img/e8afb8ef0e30a83ea01f485382f84b72.png)](https://hackaday.com/wp-content/uploads/2020/01/librepcb-mixer-schematic.jpg)

The schematic editor in action, with my simple op-amp mixer as a test project.

令人耳目一新的是，对于一个还处于酝酿阶段的项目来说，LibrePCB 团队已经努力提供了一个无缝的安装程序，而不是依赖于 git 命令或压缩档案。在 Ubuntu 系统上的安装非常直观和容易，选择目录是一个简单的过程。当开始一个测试项目时，您需要在它直接进入原理图编辑器之前设置库，正如预期的那样，可以在它和布局编辑器之间轻松切换。

这个界面给我的第一印象是，它比它的开源竞争对手更简单、更直观，作为一个从未发现自己对 KiCAD 完全放心的前 Eagle 用户，我立即感到宾至如归。我提到的学习曲线在很大程度上是不存在的，尽管不是所有的东西都在同一个地方，但是工作流和方法是足够相似的，可以毫无问题地开始。

[![My hastily-assembled 2N3904, with join-the-dots outline.](img/394cd2c53a78e05b6cd1956953a832f4.png)](https://hackaday.com/wp-content/uploads/2020/01/librepcb-parts-2n3904.jpg)

My hastily-assembled 2N3904, with join-the-dots outline.

没有任何特别要构建的东西，我直接进入一个简单的多谐振荡器来测试它的速度，然后是一个稍微复杂一点的带接地层的模拟混频器。如此年轻的软件的一个缺点立刻暴露无遗，因为它附带的组件库显然不够全面，并且在许多情况下缺少符号。没问题，事实上它给了一个方便的机会来查看封装外形和符号编辑器以创建一个新的组件。

你可以说我是老古董，但我的第一个简单测试是一个分立 2N3904 晶体管。这是一个足够简单的足迹创建，但我发现我不能创建所需的 TO-92 圆形轮廓，因为缺乏创建弧的能力。我不得不凑合着用点划线，但我会接受的。也许我应该将焊盘排列成三角形，而不是直线，但是 LibrePCB 让您可以非常容易地添加替代的足迹。它可以在一个封装中容纳各种不同尺寸和类型的相同元件，而不是将一个封装视为一个封装，例如，我的 TO-92 封装可以包含直插式、三角形和 ammopack 版本。

## 仍然可以找到一些粗糙的边缘

[![Both R1 and R2 are supposed to be 0805 SMD parts.](img/b9f278397c1b0ecb3198c07659546e44.png)](https://hackaday.com/wp-content/uploads/2020/01/librepcb-layout-resistors.jpg)

Both R1 and R2 are supposed to be 0805 SMD parts.

当我创建组件布局时，出现了一个意外问题。我在原理图中选择了 LibrePCB 的一个库存 SMD 电阻，但电路板上显示的是一个通孔元件。在组件库中检查 stock 组件的包，除了我选择的组件中的 SMD 封装之外，什么也没有发现，但是它确实存在。创建一个新的 SMD 电阻元件并用它取代股票模型带来了正确的电路板上的足迹，但显然我偶然发现了一个粗糙的边缘固有的仍然是一个阿尔法软件。

[![In places such as the Gerber creation screen, there are warnings to remind you that LibrePCB is still at an experimental level.](img/baf000f4793e939138e9fb431f8f6b08.png)](https://hackaday.com/wp-content/uploads/2020/01/librepcb-gerber-creation.jpg)

In places such as the Gerber creation screen, there are warnings to remind you that LibrePCB is still at an experimental level.

PCB CAD 软件包的目的是制造 PCB，所以接下来是运行设计规则检查并导出我的设计。写这篇文章的时候，中国的春节就要到了，为几个我不想要的项目订购 PCB 没有什么意义，但我仍然可以创建一套 Gerbers，并在 gerbv 中查看它们。

设计规则检查是版本 0.1.3 中的一个新特性，令人烦恼的是，它不会保存您对默认值所做的任何更改，但它会警告您这一点，并让您认为这将会改变。如果能够选择加载和保存不同的 DRC 设置来满足不同板房的各种需求，那就太好了。Gerber 导出非常简单，我很快就有了一组文件，加载到一个板中，完全符合我在 gerbv 中的预期。我没有理由相信，如果我把他们送到板房，我不会很快收到一套印刷电路板，而不会对我所寄的质量产生疑问。

## 它准备好迎接重大时刻了吗？

然后很有可能使用 LibrePCB 设计一个简单的 PCB，并为板房创建 Gerbers。你当然可以尝试一下，但是尽管他们已经取得了值得称赞的成就，对于一个处于早期阶段的人来说，这是一个非常有用的软件，但它还有一段路要走。会有一些 bug，很明显[在未来的版本](https://docs.librepcb.org/#projectstatus)中还有一些特性需要实现，而且库也不是很全面。前两个不可避免地会随着后续版本的发布而改进，最后一个会随着用户群的扩大而增长。

[![The view is gerbv, the EDA package is LibrePCB, the layout faux pas are all mine.](img/62cad43a0c3b6c62fec4b1c2ee48b18f.png)](https://hackaday.com/wp-content/uploads/2020/01/librepcb-gerbv-layout.jpg)

The view is gerbv, the EDA package is LibrePCB, the layout faux pas are all mine.

每当一个新的开源项目到来，做着与一个成熟的软件自由播放器相同的任务，不可避免地会有声音谴责它，好像它在某种程度上稀释了竞争对手的可用资源。我不同意这种观点，因为我认为多样性对生态系统至关重要，但值得一问的是 LibrePCB 将实现什么，它将在哪里找到合适的位置。

也许这个问题的答案会让那些担心它可能会从 KiCAD 这样的公司夺取资源的人满意，因为在使用它之后，我觉得它的优势在一个完全不同的方向。几年前，我们圈子里的默认选项是 Eagle，但将该软件包出售给 Autodesk 以及随后转向订阅模式削弱了这种优势。LibrePCB 不太可能吸引专业 Altium 用户或已建立的 KiCAD 用户，但它对于长期使用 Eagle 的用户来说易于用户界面迁移，这给了它一个 KiCAD 难以应对的机会。如果他们能够增强这种体验，并为新旧格式的 Eagle 项目提供迁移路径，我认为他们将成为赢家，并很容易成为我们在这里介绍的项目中的常见景观。

那么，应该安装 LibrePCB 吗？无论如何，安装它，了解它，如果你有相关的技能，为它做贡献。应该用它来设计 PCB 吗？你当然可以，试一试也无妨，但是由于当前版本的早期状态，你不可避免地会遇到一个限制。您是否应该放弃其他工具，将所有工作迁移到当前版本的 LibrePCB？大概不会，除非你喜欢冒险的生活。我认为 LibrePCB 是一个值得关注的，到目前为止他们已经做了非常好的工作，我认为将来有可能从它那里得到一个非常有用的软件。注意空间。