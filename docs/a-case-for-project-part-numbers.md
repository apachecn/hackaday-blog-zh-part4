# 项目零件号的案例

> 原文：<https://hackaday.com/2020/12/02/a-case-for-project-part-numbers/>

即使我们共享开源硬件的设计文件，数字文件和现实世界的机电一体化部件之间的差距仍然很大。这就是为什么我开始了个人恩怨，想办法让开源机电一体化项目的新来者更容易地完成这个转移步骤。

今天，我想透露其中一个发现:*零件号*，并展示它们如何帮助你分享你的项目，以帮助其他人复制它。把部件号想象成软件的版本号，但是是在真实的对象上。

我将展示一个在我的一个项目中使用零件号的例子，然后我将展示零件号如何为您的项目提供一些强大的社区建设功能。

## 欢乐地讲述的故事

为了让这个想法更有说服力，我把它用在了我的[开源工具更换机](https://hackaday.com/2019/11/14/jubilee-a-toolchanging-homage-to-3d-printer-hackers-everywhere/)上 [Jubilee](http://jubilee3d.com/) 。在 2019 年 10 月至 2020 年 11 月期间，我们在 Discord 服务器上建立 Jubilees 的人数从 1 人慢慢增加到 50 多人。

 [![@msds's Jubilee](img/bc6c9c02a4559e564107bc0993fcb8c1.png "msds_jubilee")](https://hackaday.com/2020/12/02/a-case-for-project-part-numbers/msds_jubilee/) @msds’s Jubilee [![@h2b's Jubilee](img/eb62651be4bf76ba79da46f39ecb73d0.png "h2b_jubilee")](https://hackaday.com/2020/12/02/a-case-for-project-part-numbers/h2b_jubilee/) @h2b’s Jubilee [![@EMRosa's Jubilee](img/f853fd67e81f4402ad7b7c5cc1052394.png "emrosa_jubilee")](https://hackaday.com/2020/12/02/a-case-for-project-part-numbers/emrosa_jubilee/) @EMRosa’s Jubilee [![@kurtblah's Jubilee](img/6f09b83901cb1c3737a6d44e83dd00f3.png "kurtblah_jubilee")](https://hackaday.com/2020/12/02/a-case-for-project-part-numbers/kurtblah_jubilee/) @kurtblah’s Jubilee [![@MiasmicTruth's Jubilee](img/5b9ca01d3bf2ef64057b62789202859d.png "miasmictruth_jubilee")](https://hackaday.com/2020/12/02/a-case-for-project-part-numbers/miasmictruth_jubilee/) @MiasmicTruth’s Jubilee [![@Xon's Jubilee](img/aafdb0831511346945467c355d097379.png "xon_jubilee")](https://hackaday.com/2020/12/02/a-case-for-project-part-numbers/xon_jubilee/) @Xon’s Jubilee [![@grabi's Jubilee](img/d5f41d4f6b484476efaf4664fd482239.png "grabi_jubilee")](https://hackaday.com/2020/12/02/a-case-for-project-part-numbers/grabi_jubilee/) @grabi’s Jubilee [![@Tsunaminaut's Jubilee](img/2045b457da8e96ddc68c98977c5b4b73.png "tsunaminaut_jubilee")](https://hackaday.com/2020/12/02/a-case-for-project-part-numbers/tsunaminaut_jubilee/) @Tsunaminaut’s Jubilee

久比利家族的一个片段

如今，Jubilee 仍然只是互联网上的[文件集合。人们建造一个需要一丝不苟地订购材料清单上的一切，3D 打印所有零件，然后逐步完成组装过程。整个过程可能需要几个月的时间，因为需要额外等待零件从海外发货。在这段时间里，设计会有一点小小的改变。对于建筑商来说，这是一个棘手的情况。随着项目的发展，他们需要决定如何发展他们的构建过程。他们是接受更新，还是继续构建他们开始时的版本？如果他们决定采用更新，他们如何跟踪他们的机器如何与最新的项目文件进行比较？](https://github.com/machineagency/jubilee)

在软件领域，这些可能是简单的答案。只需用一个简单的命令行咒语检查您正在运行的代码版本！或者检查您正在执行的文件的名称，或者您创建它的日期。所有这些答案都适用于数字文件，但在现实世界中很快就失效了。一旦我们把 STL 文件转换成现实世界的一部分，我们就失去了信息。我们正在切断带有元数据的可跟踪文件和它所代表的物理对象之间的联系。那么我们如何保持这种联系呢？一种方法是将零件号直接刻在物体上。这是我为这个项目选择的路线。

退一步说，我分享银禧的目标之一是试图给任何建造它的人一种在他们建造过程中的代理感。简而言之，随着时间的推移，Jubilee 的设计会随着人们的改进而改变。当人们构建它时，我希望他们能够对这些变化做出明智的决定。为了实现这一点，我认为人们通过检查实际的机器，而不是创建它的文件，来识别他们正在构建的机器版本是很有用的。这是零件编号背后的真正驱动力:让制造商清楚地了解他们的机器与项目的关系。

## 但是首先:一些设计理论

如果你拿起一本唐纳德·诺曼的*日常用品的设计*，零件编号如何有所帮助的想法就开始变得有意义了。在他的[一书中，你应该完整地阅读](https://hackaday.com/2020/05/29/books-you-should-read-the-design-of-everyday-things/)，诺曼提出了两个截然不同的概念，头脑中的知识*和世界中的*知识*。作为设计物的使用者，头脑中的*知识*是你需要记忆的信息，以便你可以使用所述设计物。这是说明书里最重要的内容。*世界上的知识*也是你需要知道才能使用对象的信息，但它不知何故依附于对象本身，所以你不需要去死记硬背。为了实现这个想法，考虑将一些设备插入视频投影仪的背面，如下图所示。哪个输入是哪个？*

[![](img/3033349663576a8981919eb2ea4e91b7.png)](https://hackaday.com/wp-content/uploads/2020/11/projector_with_markings.jpg)

with embedded input labels.

[![](img/38dcb0de9550921ccdb6285255315294.png)](https://hackaday.com/wp-content/uploads/2020/11/projector_without_markings.jpg)

without embedded input labels! Which would you rather use?

谢天谢地，最上面的那个是有标签的；那就是*世界上的知识*。但是底下的不是，手册里有。那是*脑袋里的知识。*你更愿意使用哪一种？虽然第二个看起来更干净，但第一个让我扔掉了说明书——或者根本不需要！这就是刻有零件号的想法。世界上的*知识*让构建者确切地知道他们手里拿的是什么，以某种方式让他们追溯到创建它的文件。

## 创建零件编号方案

现在我们知道了零件编号是如何帮助我们的，让我们来讨论一下如何将它应用于 Jubilee 和一般情况。我的理解是，当涉及到零件编号方案时，业内人士分为两个阵营。要么(1)您的零件号只是一个随着每个新零件而递增的数字，要么(2)您的零件号具有结构化的*字段*，每个字段都有特定的含义。第一个例子就是这样一个数字序列: **000001** 。第二个可能是这样的: **07-BED-04-MKS-MRW** 。

我认为两者都有位置和案例；只是看情况。如果您的零件号不需要人工阅读或可以用计算机快速查找，简单的数字零件号就有意义。见鬼，你甚至可以把它编码在贴在零件上的条形码上，使查找过程更容易。如果零件编号方案的范围不断扩大，出现了您无法预先确定的新类别，枚举可能也有意义。

但是，如果您的零件号需要某种人类可读的含义，第二种选择可能是可行的。这非常适合禧年。首先，项目范围定义明确。我们知道机器不会有越来越多的类别。第二，也是更重要的一点，项目新手可能需要阅读零件号。

为了制定零件编号方案，Jubilee 社区的一些人在 Github 上发起了一场讨论[。计划是将该方案应用到每一个非现成的部分。在这里，这意味着每一个 3D 打印和加工的零件都会直接嵌入一个零件号。这次谈话的关键是一个悬而未决的问题:*什么有意义的信息值得编码到零件号中让其他人阅读？*我们想出了一些外卖。对于所有部分来说，版本很重要，拥有某种简短的独特“签名”来轻松识别它也很重要。对于机械零件来说，“谁制造的”很重要。](https://github.com/machineagency/jubilee/issues/11)

除了 Github 上的对话，Jubilee 的 Discord 服务器上的其他情况也在推动识别部件，即调试其他构建者的设置。首先，将不同版本的机器零件混合在一起并不总是可行的，因此拥有混合批次零件的制造商会发现自己处于组装说明要求他们做一些不可能的事情的场景中。

在其他情况下，一些人带着制造质量导致组装或性能问题的加工零件来了。但是，如果不知道这些加工零件来自哪里或它们是如何制造的，就需要进行额外的交谈来发现是否有任何加工过程对这些问题负责。简而言之，预先拥有任何形式的*可追溯性*都将是一个额外的好处，可以在调试其他人的 Jubilee 设置时简化一些步骤。

几经周折，我选定了一个如下所示的方案:

**[子组件]–[零件 id +参数]–[修订版]–[制造工艺+材料]–[谁制造的]**

有一个简短的版本，看起来像这样:

**[零件 id +参数]–[修订版]**

第一个选项是完整的零件号。第二个是需要在某个地方安装到零件上的最低要求。大多数 3D 打印零件只是嵌入了零件侧面的简短零件编号。这里有一个镜头，这些看起来像在少数几个部分的行动。

 [![IMG_20201012_185332 (1)](img/9cb0bee0dcc85dccfb4f9d0de8f64d65.png "IMG_20201012_185332 (1)")](https://hackaday.com/2020/12/02/a-case-for-project-part-numbers/img_20201012_185332-1/)  [![IMG_20200320_163231 (2)](img/7bc672fb70ad0ebc9ce39d6c13b7f633.png "IMG_20200320_163231 (2)")](https://hackaday.com/2020/12/02/a-case-for-project-part-numbers/img_20200320_163231-2/)  [![IMG_20201113_200953](img/0aa4baca2621dde1b799d7668985e128.png "IMG_20201113_200953")](https://hackaday.com/2020/12/02/a-case-for-project-part-numbers/img_20201113_200953/)  [![IMG_20201113_201110](img/8ebe42edba3b67bc99cdc67903448004.png "IMG_20201113_201110")](https://hackaday.com/2020/12/02/a-case-for-project-part-numbers/img_20201113_201110/) 

最后，我应该提一下，银禧的零件号是项目专用的。一个不同的项目意味着一组不同的零件号(尽管我可能会重用[相同的方案](https://jubilee3d.com/index.php?title=Part_Numbers))。但在这种情况下，我们只需要一种方法来帮助禧年建筑者知道他们是从哪里开始建造的，并以一种非常具体的方式相互交流。

### 分散制造的零件

随着 Jubilee 的设计成熟，一些机械师实际上开始制造小批量的零件，以出售给不断增长的建筑商群体。结果是，设计变得更容易自我采购，因为如果你自己不能制造，你可以购买机械零件。

零件编号方案设定后，我联系了这些机械师，询问他们是否愿意在零件上蚀刻零件编号，并在他们的网站上列出零件编号。他们欣然同意。这里，每个供应商都有一个唯一的零件号，除了最后几个字段之外，其他都很相似。这些最后的部分标识了部件的材料和制造商。

 [![The Spec](img/3a94dce5aedeec3eb1ac2cbc5121f6b2.png "build_plate_spec")](https://hackaday.com/2020/12/02/a-case-for-project-part-numbers/build_plate_spec/) The Spec [![a 713Maker Bed](img/edabd95b0cf43d3b92b1f1f96e102160.png "IMG_20201113_213757")](https://hackaday.com/2020/12/02/a-case-for-project-part-numbers/img_20201113_213757/) a 713Maker Bed [![A Mandala Rose Works Bed](img/e18dc4b324acaeae4742b67daa4c95c8.png "IMG_20201113_214140")](https://hackaday.com/2020/12/02/a-case-for-project-part-numbers/img_20201113_214140/) A Mandala Rose Works Bed

因此，尽管 713 制造商和 T2 曼陀罗玫瑰工厂都生产铝制床板，零件编号却能告诉我们它们是由什么制成的，是谁制造的。其次，拥有一个零件号也可以作为新的禧年建设者的“资格”。这是一个隐含的承诺，即从这些地方制造的零件有足够的社区支持，值得以一些项目标识的形式得到一些认可。最后，如果这些零件中的任何一个引起问题，社区中的任何构建者都可以使用零件号来联系制造该零件的机械师以寻求支持。这是真的，即使他们没有自己制造机器，而是从别人那里买了一台组装好的机器。

### 印刷零件号易读性

至于打印设置，我发现当文本打印在零件的侧壁上时，打印的零件号最容易阅读。即使零件号只有 25 层线粗，该点也能使零件号清晰可辨。

 [![IMG_20201113_201219](img/db1566c5f27877c178538c9be70552c1.png "IMG_20201113_201219")](https://hackaday.com/2020/12/02/a-case-for-project-part-numbers/img_20201113_201219/)  [![IMG_20201113_201412](img/222ade2505697bc18e3f9842a931b59f.png "IMG_20201113_201412")](https://hackaday.com/2020/12/02/a-case-for-project-part-numbers/img_20201113_201412/) 

此外，在大多数类型的 3D 打印机上，这一面的打印似乎相当清晰——即使是像 Ender 3 Pro 这样的廉价机器。虽然我确实尝试过在 3D 打印零件的顶部和底部打印数字，但小写字母的特征就是不一致，这使得零件在一系列机器上打印变得更加困难。

## 使用零件号进行设计

这几天，每次在 [GitHub 发布](https://github.com/machineagency/jubilee/releases)之间修改一个零件，我都会更新零件号。实际上，这很容易跟踪。如果我在发行版之间编辑一个零件，我只需勾选数字，并以首选的打印方向重新导出 STL。零件号以元数据的形式存储在模型文件中，但是如果我不知道从哪个编号开始计数，我可以只查找上一个版本的 STL。这意味着 *STL 文件保持它们的名字*，但是它们的内容改变了。这让我们免去了额外的簿记工作，因为像[维基](https://jubilee3d.com/index.php?title=3D_Printed_Parts)这样的地方的零件超链接不需要在每次零件号改变时都改变。这也符合软件惯例。每次我们改变一个文件，我们不会给它一个新的名字。版本控制软件为我们跟踪文件的历史。如果您使用 Git 这样的工具来跟踪设计文件，那么对于表示硬件的设计文件来说也是如此。有趣的事实！GitHub 实际上会[呈现两个 STL 文件](https://github.blog/2013-09-17-3d-file-diffs/)的差异，如果你挖掘它们的话。

![](img/4902ac443f538bf1780e22084bbaad3e.png)

Github’s representation of this part’s changes between the last two commits.

任何时候我在一个版本之间改变我的部分，我也会在项目的 [Changelog](https://github.com/machineagency/jubilee/blob/master/CHANGELOG.md) 中做一个记录。当 Jubilee builder 遇到一个新版本时，他们可以找到一个快速列表，列出所有以某种方式发生变化的非库存部分。这也是总结该零件上的几何图形变化及其原因的地方。这样，他们可以自己决定升级到新零件是否值得重新组装他们的机器。

## 使用零件号进行通信

> 还记得组装说明中的一部分吗？是那个*flibbity-jibbit-short-left-hand-edition-version-3*？

给事物命名很难。描述它们更难。有了铭刻的零件号，交流设计变得更加容易。在项目建设者之间*和*在建设者和设计师之间更容易。这有两个原因。首先，我们不需要查找任何零件名称；它们直接写在零件上！当我们想就这些部分进行对话时，这非常有用。第二，该名称对于该部件的版本来说是高度特定和唯一的。通过用零件号指代零件，我们所谈论的内容就不会有歧义。

结果是，交流中的一些打嗝就这样“消失”了如果有人想说组装过程中的零件，不用费劲描述，也不用查名字；他们只是检查它们的数量。第二，如果有人用不兼容的部分版本进行构建，我们可以通过对照 Changelog 交叉引用它们来发现它。当您的 Discord 社区有超过 1000 名不同技能水平的人请求帮助构建不同的机器版本时，消除任何沟通摩擦是获得更轻松调试体验的关键。

最后，真正特别的是，零件编号如此具体，以至于不是最初项目设计者的建造者可以进行对话，而不需要设计者澄清它们之间零件的差异。那是强大的。添加零件号消除了设计师作为澄清设计细节的调解人的需要。该设计直接与社区合作，而不是从最初的设计者那里提炼。

## 部分号码建立社区，部分

我承认:想出一个编号方案，然后在项目进行到一半时实现它，这是一项额外的工作。所以这里有一个很好的问题:如果机器已经为你工作了，为什么还要花费这么多额外的努力在项目中添加一些不会直接增强你的机器的东西呢？我认为答案在于分享。

说实话，我不知道换刀机以后会有多普及。但我知道设计它们很难。最后，我真的希望看到人们在他们的基础上构建有趣的应用程序。但是，并不是每一个兴奋地想玩游戏的人都有时间或技能来设计一个。所以我现在试着问自己的问题是:*我怎样才能带你一起走？*

我认为零件号是一种方法。它们是一种为构建您的项目的所有人员提供一种通用语言的方式，以帮助回答新成员的问题。这是一种帮助他们识别机器是否存在与设计相关的问题或与其制造商收到的修改相关的问题的方法。虽然我不能跟上新构建者提出的每个问题，但社区可以！用精确的语言武装他们，在一定程度上是我们让他们更有能力维持增长的方式。随着越来越多的声音能够回答你的构建问题，你也可以得到一个工作的机器。因此，即使你不能或不想从头设计一个好的工具更换平台，你仍然可以在它的基础上构建。

我希望我能得到零件号，但我不能。工业界的工程团队一直在使用它们来分担和委派大型项目的复杂性。如何阻止我们开源硬件黑客借用他们的一些方法来建立社区？

## 太好了——我可以从哪里了解更多信息？

嘿，不要相信我的话。早在 Jubilee 发行的早期，就有一些人向我推荐零件号。最终，这个视频也登陆了 Discord 服务器，它确实击中了论点的要害。让 Wintergatan 带你进行一次有趣的讨论，讨论他的任务与他的机器的复杂性之间的争论。

 [https://www.youtube.com/embed/zVyEsMiwvVc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zVyEsMiwvVc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

