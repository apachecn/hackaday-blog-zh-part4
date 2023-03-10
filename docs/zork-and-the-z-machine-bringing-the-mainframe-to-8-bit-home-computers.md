# Zork 和 Z-Machine:将大型机引入 8 位家用计算机

> 原文：<https://hackaday.com/2019/05/22/zork-and-the-z-machine-bringing-the-mainframe-to-8-bit-home-computers/>

自从有了电脑，电脑游戏就存在了。虽然可能很难相信，基于文本的冒险游戏 Zork 是当时的堡垒之夜。但佐克不仅仅如此。由于可移植性和大小的原因，Zork 本身是用 Zork 实现语言(ZIL)编写的，大量使用了面向对象编程的全新概念，并在虚拟机上运行。这一切都发生在 1979 年。他们使用了书中的每一个技巧，将尽可能多的地下帝国装入只有 32 kB 内存的计算机中。但是，Zork 不仅仅是一部技术杰作，它还是电脑游戏史上不可错过的里程碑。但它不是凭空出现的。

![DEC PDP-10 Flip Chip module](img/99996b6d58c3ce40e7c0cff2a8898e92.png)

DEC PDP-10 Flip Chip module

计算机革命在第二次世界大战期间刚刚站稳脚跟，在 20 世纪 50 年代和 60 年代没有消退的迹象。越来越多的企业和大学可以购买到更便宜的计算机系统。麻省理工学院的计算机科学实验室(LCS)很幸运地与 ARPA 有联系，这使得麻省理工学院的 LCS 和人工智能实验室(以前是项目 MAC 的一部分)可以访问大量的计算资源，主要是以系统的形式。

结果:麻省理工学院动态建模小组(LCS 的一部分)的学生可以使用一台 [PDP-10](https://en.wikipedia.org/wiki/PDP-10) KA10 主机——当时很重的铁。虽然这款 PDP-10 是 1968 年的原版，带有分立晶体管[倒装芯片](https://en.wikipedia.org/wiki/Flip_Chip_%28trademark%29)模块和绕线，但它已经过[的大幅修改](https://github.com/PDP-10/its/issues/181)，增加了虚拟内存和分页支持，以扩展原有的 1,152 kB 核心内存。运行麻省理工学院开发的[不兼容分时系统](https://en.wikipedia.org/wiki/Incompatible_Timesharing_System) (ITS)操作系统，这是一个高性能的多用户系统。

自然，它主要用于玩游戏。

## 你准备好冒险了吗？

1977 年春天，一款名为[巨大洞穴探险](https://en.wikipedia.org/wiki/Colossal_Cave_Adventure)的游戏来到了麻省理工学院。这个游戏是第一个[互动小说](https://en.wikipedia.org/wiki/Interactive_fiction)电脑游戏，为玩家提供了一个文本冒险，涉及一个据说充满宝藏的大洞穴系统。令人想起“选择你自己的冒险”书籍，玩家将做出选择，带领他们穿过洞穴的房间，要么成功找到宝藏并活着逃离，要么遭遇不合时宜的死亡。

受这个游戏的启发，LCS 的一群学生认为他们可以做得比这个斯坦福开发的项目更好。他们发现的主要弱点是 Adventure 是用 FORTRAN 实现的，这种语言并不以其强大的动态文本处理功能而闻名，更不用说交互式小说游戏的需求了。正因为如此,《冒险》本质上对整个游戏进行了硬编码，限制了灵活性，并使游戏的扩展和维护变得复杂。

在冒险中，每个房间都有一个数字 ID，并在表格中有相关的描述。另一个表定义了它的简短描述。另一个表格使用房间的数字 id 列出了这些房间相对于其他房间的位置。这意味着，为了添加一个房间，必须修改所有这些表，注意不要因为这些更改而导致任何问题。

## 黑客竞争

![](img/b7a9883938b6f01a27c984d6fe52a5d3.png)

利用当时存在于 LCS 和人工智能部门的自然语言经验，是[戴夫·莱布林](https://en.wikipedia.org/wiki/Dave_Lebling)首先使用 LISP 衍生的 [MDL](https://en.wikipedia.org/wiki/MDL_%28programming_language%29) 编程语言，组装了一个简单的解析器和一个类似于 Adventure 的游戏引擎的开端。利用 MDL 强大的自然语言处理能力， [Marc Blank](https://en.wikipedia.org/wiki/Marc_Blank) 、 [Bruce Daniels](https://en.wikipedia.org/wiki/Bruce_Daniels) 和 [Tim Anderson](https://en.wikipedia.org/wiki/Tim_Anderson_%28Zork%29) 然后在 Lebling 的努力基础上[创造了](https://www.filfre.net/2012/01/zork-on-the-pdp-10/)第一个原型游戏，最终成为我们今天所知的“Zork”游戏。

Zork 的革命在于，由于 MDL 强大的自然语言特性，它可以理解整个句子，这与 Adventure 的简单命令相反，在 Adventure 中“LAMP GET”和“GET LAMP”是等价的。它可以理解完整的句子，甚至可以将多个句子(命令)串成一个句子。强大的解析器，加上使用 MDL 以面向对象的方式建模新房间的便利性，意味着在解析器和游戏引擎编写完成后，世界实际上可以任意扩展。

Zork 中的一个房间可以用如下简单的代码来定义:

`<ROOM "WHOUS"
"This is an open field west of a white house, with a boarded front door."
"West of House"
<EXIT "NORTH" "NHOUS" "SOUTH" "SHOUS" "WEST" "FORE1" "EAST" #NEXIT "The door is locked, and there is evidently no key.">
(<GET-OBJ "FDOOR"> <GET-OBJ "MAILB"> <GET-OBJ "MAT">)
<>
<+ ,RLANDBIT ,RLIGHTBIT ,RNWALLBIT ,RSACREDBIT>
(RGLOBAL ,HOUSEBIT)>`

这从游戏开始就定义了“白宫”,以及这个房间的出口、出口的特殊属性(例如一扇锁着的门)和房间里的物体。这可确保房间的所有属性(包括描述、简短描述、属性和标记)都在一个位置。然后，游戏引擎可以切换房间上的单个标签(位)，保存所有房间及其当前状态的中央数据库。在游戏设计过程中，管理哪些房间是相连的是使用正确的名称，而不是表格中的数字 id。

## 轰动的演出

可以这么说，Zork 在大型机上绝对出色。由于其他感兴趣的游戏玩家的普遍需求，它被移植到 PDP-10 的更广泛的 DEC[TOPS-20](https://en.wikipedia.org/wiki/TOPS-20)OS 上。尽管 Zork 的开发者们慷慨地免费赠送了这款游戏，但他们确实以只读、加密版本的形式发行了这款游戏。他们甚至将 Zork 的源代码存储在 ITS 大型机的一个安全文件夹中，为此他们必须修补完全开放且不安全的 ITS 大型机操作系统。

![](img/01010c9e92c2637f13a1224132ff3b28.png)

在计算机历史上的这个时候，世界上的计算机仍然相对较少。随着 1977 年像 TRS 80 T1 和 T2 苹果 2 T3 这样的电脑的出现，家用电脑的概念才刚刚开始深入人心，尽管与当时美国各地学生用于文本冒险的大型机相比，这个系统的局限性令人难以置信。将像 Zork 这样的 1 MB 可执行程序移植到家用电脑上的想法似乎有些牵强。

当家用电脑还很少的时候，向普通消费者销售软件也是一个新的概念。这是雅达利 2600 刚刚上市的时候，这是第二代游戏机，通过使用插件可以扩展到多个游戏。这是一个新的市场，[在麻省理工学院、斯坦福大学和其他学生中有许多关于开放黑客文化和商业软件世界的问题。有些人，比如 T4·理查德·斯托尔曼·T5，从他们在麻省理工学院的学生时代起就没有改变过他们的立场。](https://www.filfre.net/2012/01/the-birth-of-infocom/)

随着 Zork 开发人员的毕业，[他们意识到](https://web.archive.org/web/20060427000213/http://www.csd.uwo.ca/Infocom/Articles/NZT/zorkhist.html)随着 Zork 的成功，他们有了一个将它商业化的机会，将他们的生活和职业带入一个与他们最初目标完全不同的方向。Infocom 公司成立于 1979 年 6 月 22 日，几乎没有遇到什么阻碍。

## 现在我们只需要把它移植过来

这仅仅留下了将 Zork 从 PDP-10 主机系统转移到那些极小的家用电脑上的微小细节；此时，Infocom 实际上还没有任何东西可以出售。他们考虑了各种可以在家用电脑上运行的游戏创意，但移植 Zork 太有意义了。他们必须解决的问题是，如何将 1 MB 基于 MDL 的游戏代码加载到内存为 32 kB(或更少)且存储量相对不足的微机上。

他们也不想将游戏单独移植到 TRS-80、Apple II 或任何即将推出的新系统上。如果可以使用现有的 MDL 源代码会怎么样？这就是后来众所周知的 [Z-Machine](https://en.wikipedia.org/wiki/Z-machine) 设计的开始。

当然，最初让 Zork 适合微型电脑的方法是通过删除内容让游戏变得更小。经过大量的剪辑，他们有了一些接近冒险的东西。然后他们对 MDL 做了类似的事情，删除了 Zork 不需要的所有特性。这创建了 [Zork 实现语言](https://archive.org/details/Learning_ZIL_Steven_Eric_Meretzky_1995) (ZIL)，他们可以干净地将 Zork 移植到 MDL。ZIL 编译器能够生成比 MDL 编译器小得多的二进制文件。

看看《ZIL》中对佐克黄铜灯笼的描述，我们可以看到它比 MDL 更容易阅读:

`<OBJECT LANTERN
(LOC LIVING-ROOM)
(SYNONYM LAMP LANTERN LIGHT)
(ADJECTIVE BRASS)
(DESC "brass lantern")
(FLAGS TAKEBIT LIGHTBIT)
(ACTION LANTERN-F)
(FDESC "A battery-powered lantern is on the trophy
case.")
(LDESC "There is a brass lantern (battery-powered)
here.")
(SIZE 15)>`

![](img/c0fd1980cbad48db2fb3aadf335c2ae6.png)

这当然很棒，但这仍然没有让佐克在 TRS-80 上跑起来。在这一点上，他们当然可以为每个平台编写一个 ZIL 编译器，以及一个 ZIL 运行时，然后花很多时间在每个目标平台上调整每个游戏。相反，他们选择编写这个虚拟机:Z-Machine。本质上是一个文本冒险游戏的[理想平台](http://inform-fiction.org/zmachine/standards/index.html)，直接支持 ZIL 二进制，也实现了许多优化，其中最重要的是将字符打包成 5 位，让人想起[博多代码](https://en.wikipedia.org/wiki/Baudot_code)。

通过所有这些优化、一个虚拟机和一种定制编程语言，他们设法将 Zork I 的精简世界压缩到一个只有 77 kB 的“故事文件”中，连同解释器(VM)。由于这对于当时主流微机的 32 kB 来说还是太大了，所以 VM 实现了一个虚拟内存系统，只将动态数据(变量)加载到 RAM 中，任何静态数据(文本)只在需要时从软盘中读取。

## 走向未来

![](img/5fda33d3eb7c314476849fcfbbacc4b0.png)

Apple II 有 140 kB 容量的软盘，TRS-80 有 180 kB，这意味着空间问题已经解决。只有解释器需要针对目标平台进行优化，这意味着对于所有未来的 Infocom 游戏，同一个解释器可以用于每一个发布的游戏，而不必将其移植到单独的平台。他们有更多来自主机版本的 Zork 的内容。他们准备拍续集。

在 Zork I 取得商业成功后，他们继续发布从 Zork II 和 Zork III 形式的原始主机版本中删除的部分。年复一年，Zork I 的销量一直在上升，它成为了新系统中的必备游戏。新的 Z-Machine 版本被开发出来，为更先进的游戏增加了额外的功能。今天[我们仍然可以享受](http://www.ifwiki.org/index.php/Z-machine) Infocom 游戏而不必担心兼容性问题:Zork 的 [MDL 源代码以及其他经典 Infocom 游戏](https://github.com/historicalsource/zork)的[源代码已经发布。如果你已经有一段时间没有玩过 Zork 了，或者从来没有玩过，试试看。毫不夸张地说，20 世纪 70 年代美国大学的一群黑客很可能定义了视频游戏和互动故事的世界。](https://github.com/historicalsource?tab=repositories)