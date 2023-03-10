# 开放 3D 引擎:亚马逊的旧衣服还是一个真正令人兴奋的游戏引擎？

> 原文：<https://hackaday.com/2022/01/10/open-3d-engine-amazons-old-clothes-or-a-game-engine-to-truly-get-excited-about/>

最近，亚马逊[宣布](https://aws.amazon.com/blogs/gametech/open-3d-engine/)他们将开放 3D 引擎和他们[亚马逊贮木场](https://en.wikipedia.org/wiki/Amazon_Lumberyard)游戏工具背后的相关资源。由于 Lumberyard 基于 [CryEngine](https://en.wikipedia.org/wiki/CryEngine) 3.8 (~2015 年份)，这就提出了一个问题:这个新的开源引擎——创造性地命名为*开放 3D 引擎*([O3DE](https://en.wikipedia.org/wiki/Open_3D_Engine))——是否是 CryTek 引擎的开源版本，以及这给我们这些喜欢摆弄 2D、3D 游戏和类似游戏的人带来了什么。

当阅读营销材料时，人们可能会认为 O3DE 是自切片 3D 面包以来最好的东西，是亚马逊给未洗过的大众的仁慈礼物，以将他们从 Unity 和 Unreal Engine 等专有引擎强加给他们的枷锁中解放出来。然而，仔细观察就会发现，O3DE 是 Lumberyard，但是, [Lumberyard 的许多部分都被替换了,](https://www.reddit.com/r/gamedev/comments/oez1tw/amazon_lumberyard_is_dead_long_live_open_3d/),包括仍在从旧的 CryEngine 代码重写过程中的渲染器。

## 一个好的游戏引擎是由什么组成的？

我自己的游戏开发尝试是从半条命引擎和阀门[锤子编辑器](https://half-life.fandom.com/wiki/Valve_Hammer_Editor)以及末日地图编辑器开始的。这意味着在遇到今天的游戏引擎及其工具之前，已经设定了一些期望。在 20 世纪 90 年代末，使用 Hammer editor 的开发体验基本上是所见即所得，当我几年前刚刚开始使用虚幻引擎 4 (UE4)时，这是非常相似的体验，使其相对容易地投入运行。

安装 UE4 需要几个步骤:在[使用安装程序安装](https://docs.unrealengine.com/4.27/en-US/Basics/InstallingUnrealEngine/)Epic launcher 并使用 Epic Games 帐户登录后，只需点击几下就可以安装 UE4 的任何可用版本。之后，向导允许使用可选的模板创建新的游戏项目。然后，这将为项目(也是游戏)创建一个专用的编辑器，因此您可以在编辑它的同时拥有一个可以与之交互的实时预览窗口。

要构建游戏，您只需按下一个按钮，就可以推出一款支持多种目标平台的游戏。从本质上来说，这种体验体现了一个优秀游戏引擎最基本的特征:无需借助引擎工具或构建系统就能创建游戏。许多用户可能是图形艺术家或类似的人，他们对他们正在使用的工具的内部没有什么兴趣。

在这里，UE4 的体验相对轻松:使用 Blueprint object 系统，您可以在图形编辑器中连接复杂的游戏和游戏逻辑，无需编写代码，尽管基于 C++的开发对于各种级别的定制都是可能的。

如果我们把这个复杂的分级系统作为一个好的游戏引擎和相关工具的黄金标准，O3DE 和它的主要竞争对手(虚幻引擎，Godot 和 Unity)相比如何？乍一看，它们似乎非常相似，都是用 C++编写的。最显著的区别可能在于它们支持扩展引擎特性的语言。

这里 Unity 的脚本 API 支持 C#，Godot 提供 GDScript(类似 Python)以及 C#和 C++。虚幻引擎是用 C++扩展的，O3DE 也是。这很好，但是使用它们是什么样的呢？

## 快速入门

在我们选择的平台上安装开发工具之前，我们需要检查系统需求。对于 O3DE [，这些是](https://o3de.org/docs/welcome-guide/requirements/):

*   Windows 10 1809 或更高版本，或
*   Ubuntu 20.04 以上。

这[与 UE4 的最低](https://fixingport.com/unreal-engine-4-system-requirements/)[要求](https://docs.unrealengine.com/4.27/en-US/Basics/InstallingUnrealEngine/RecommendedSpecifications/)Windows 7 或更高版本，或 MacOS 10.9 (Mavericks)或更高版本形成对比，这两个版本都提供二进制安装程序。对于 Linux 来说，引擎必须从源代码构建[，但是](https://docs.unrealengine.com/4.27/en-US/SharingAndReleasing/Linux/BeginnerLinuxDeveloper/SettingUpAnUnrealWorkflow/)[应该可以与 Ubuntu 16.04 LTS 和更高版本以及一系列其他 Linux 发行版一起工作](https://unrealcommunity.wiki/building-on-linux-qr8t0si2)。对于 Unity，系统要求与[相似](https://unity.com/download)，需要 Windows 7 SP1+，MacOS 10.12+和 Ubuntu 16.04+或 CentOS 7。

虽然 Unity[不要求](https://support.unity.com/hc/en-us/articles/360061586571-What-is-the-Unity-Hub-)使用其 Unity Hub 应用程序(到目前为止),但它大力宣传它是管理 Unity 项目和许可证的一种中央方式，类似于 UE4 的 Epic Games Launcher 应用程序。这是一种财富还是一种负担，很大程度上取决于一个人的工作流程。对于管理具有各自引擎版本的多个并发项目并保持这些版本的更新，拥有这样一个中央工具是非常有用的。

与 Unity 和 UE4 不同的是，Godot 对网站没有任何强有力的系统要求，应该可以在任何支持所需编译器和依赖项的平台上编译。提供的二进制文件来自一个档案，没有安装程序，并独立运行，这可能是这些引擎中最容易安装的。

在 Windows 上安装 O3DE [时，会安装 O3DE 编辑器和项目管理器。对于 Linux(前面提到的 Ubuntu 20.04 或更高版本)，有一个 DEB 包你](https://o3de.org/docs/welcome-guide/setup/installing-windows/)[可以下载后安装](https://o3de.org/docs/welcome-guide/setup/installing-linux/)。通过[项目经理](https://o3de.org/docs/welcome-guide/create/creating-projects-using-project-manager/)，可以创建和构建新项目。除了支持的开发平台数量有限之外，这个工作流看起来还比较有可比性。

如果一个开发环境不能完成所要求的任务，那么安装这个开发环境就没有什么意义了，我们应该后退一步，看看这些引擎可以用于哪些平台的开发。这将告诉我们是否有兴趣花时间和精力去学习它。在这里，O3DE 相当平淡，至少在文档方面是这样，或者说缺少文档。

虽然列出了 Android 和 iOS 移动平台，但很难找到具体的信息，就像 MacOS 一样，在撰写本文时，只列出了 Linux 的一些信息[。这与 Godot 形成对比，Godot 在](https://o3de.org/docs/user-guide/platforms/linux/)[功能列表](https://godotengine.org/features)中列出了其平台，包括从桌面、移动、网络和控制台平台的一切，包括[关于如何为这些平台构建的详细](https://docs.godotengine.org/en/latest/development/compiling/index.html)信息。

对于 [Unity](https://support.unity.com/hc/en-us/articles/206336795-What-platforms-are-supported-by-Unity-) 和 [UE4](https://docs.unrealengine.com/4.27/en-US/SharingAndReleasing/) ，我们看到了类似的目标平台和文档提供。O3DE 似乎主要局限于常见的桌面平台和移动平台，尽管文档中很少提到支持哪些功能。O3DE 目标的[构建指令](https://docs.o3de.org/docs/user-guide/build/configure-and-build/)表明，在能够为任何目标构建之前，需要手动配置 CMake 并运行这个构建脚本生成器。CMake 是否比 Godot 使用 SCons 更好是另一个问题，但它确实突出了 U3DE 和 Godot 都需要的技术知识。

## 文档和支持

不可否认的是，Unity，UE 和 Godot 在游戏开发中非常受欢迎，前两者也有强大的商业支持。所有这些背后都有一个庞大的社区，这些产品的(相对)开放性使之成为可能。所有这些都可以免费使用，并有多年的发展，从 AAA 到独立游戏的度量负载。

这样做的结果是，即使文档在某些方面不清楚或者遗漏了一些细节，社区也有很好的机会帮助解决任何问题。这与以前被称为 Lumberyard 的引擎形成了鲜明的对比，在撰写本文时，最新版本的[发行说明](https://o3de.org/docs/release-notes/archive/21-11-release-notes/)提到该引擎仍在开发中，人们不应期望用它来构建一个生产就绪的产品。

这种测试版的感觉在今天的文档中仍然存在，没有其他引擎文档的冗长。考虑到亚马逊贮木场引擎在过去几年中不受欢迎，这一切都不足为奇。不管怎样，这些发现表明了人们对当今 O3DE 的期望。

所有这些都提出了这个项目的未来会是怎样的问题。它会成为 Godot、Unity 或者——但愿不会如此——UE4/5 的竞争对手吗？

## 支付账单

像 Unity 和 UE 这样的产品的最大资产也许是它们可以共存于 AAA 游戏和三流开发者以及爱好者之间。这大部分是由两者的许可系统处理的。对于 UE4 来说，这意味着[可以免费使用](https://www.unrealengine.com/en-US/download)，如果引擎被用于游戏开发以外的任何用途，也没有版税。如果你用 UE4 制作了一款票房超过 100 万美元的游戏，超过 100 万美元的部分将收取 5%的版税。

对于 Unity，个人计划是免费的，学生计划也是免费的。如果一年的收入超过 100，000 美元，则适用 Plus 计划，每个座位 399 美元。这些计划[随着收入的增加而增加](https://store.unity.com/compare-plans)(下一个>20 万美元/年)。像 UE4 一样，如果你不把软件商业化，就不需要付费。这与 Godot 形成对比，Godot 没有商业计划，但是除了代码贡献之外，它还接受[金钱奖励](https://en.wikipedia.org/wiki/Godot_(game_engine))和捐赠。

虽然许多工作室都有自己的内部游戏引擎，但虚幻引擎和 Unity 都看到他们的产品被用于各种商业软件，所有这些都确保了即使是小开发者和爱好者也能从为这些商业客户实现的前沿功能中受益。虽然 Lumberyard 理论上可以成为类似于 Unity 和 UE4 的东西，但它似乎没有获得与这两个产品几乎相同的资金水平。

## 又一个引擎

尽管有关于 O3DE 的崇高主张，但很难忽视房间里的大象。在亚马逊的游戏开发雄心被大幅削减后，其基于贮木场的[新世界](https://en.wikipedia.org/wiki/New_World_(video_game))游戏仅获得中等评价，而在后台贮木场实际上被砍掉了。因此，O3DE 似乎更像是一种愤世嫉俗的方式，来削减开发一个看似奄奄一息的游戏引擎的成本。

也许最好的结果是，像 Godot 这样的现有项目可以从 O3DE 引擎中获取有用的部分，这将为用户带来两全其美的好处:一个完全免费和开源的游戏引擎，拥有体面的工具和一个支持它的大型社区。这是否包括移植 O3DE 中的 AWS 云支持模块，谁也说不准。

然而，归根结底，开发人员在 OSS 世界中的时间是宝贵的。将它分散在越来越多的类似项目中似乎不是很有利。集中资源似乎是最明智的做法。

至于对于只想做游戏的人来说，自己做还是和几个哥们一起做最合适？UE4 或 Unity，如果你对构建系统和工具的内部修补不感兴趣的话，否则 Godot 似乎是一个适合任何东西的平台，从简单的手机游戏到复杂得多的桌面游戏，甚至是主机游戏。

但是 O3DE？在接下来的几个月或几年里，我们可能会看到它的结局，以及它是否能成为一款可以制作游戏的产品。直到最后一只海狸唱它的绝唱，它才结束。

[标题图像:打开 3D 引擎编辑器，其中包含游戏 Deadhaus Sonata open 中的 Amazon 着色器语言文件和资源。(信用:O3DE 项目)]