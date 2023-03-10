# 感兴趣的输入:我正在构建一个 ErgoDox！

> 原文：<https://hackaday.com/2020/05/06/inputs-of-interest-im-building-an-ergodox/>

我已经用了我的 [Kinesis Advantage 键盘](https://hackaday.com/2020/03/03/inputs-of-interest-my-first-aggressively-ergonomic-keyboard/)两个月了，我很喜欢它。如果可以的话，我再也不会回到普通键盘了。

然而，它也有一些缺点。最大的一点是，两边的分裂距离是固定的。它没有樱桃 MX 蓝色(虽然棕色加固件哔哔声很好)。它没有层次，真的——只有右手下面的一个十键。老实说，它不太便于携带。

[![](img/abe8406d1af11d2592513a2d9bc65ad1.png)](https://hackaday.com/wp-content/uploads/2020/04/nuclear-ergodox.png)

ErgoDox with Nuclear Data keycaps via [geekhack](https://geekhack.org/index.php?topic=42772.300)

我带着 Kinesis 去了一家咖啡店几次，直到它们都变成了免下车服务，在公共场合把它放在一辆四顶敞篷车上让我意识到它到底有多大，有多吵。

所以我正在制作一个 [ErgoDox 键盘](https://www.ergodox.io/)。我真正想做的是 Dactyl — [,是 ErgoDox](https://github.com/adereth/dactyl-keyboard) 的弯曲变体——但我不能在没有首先构建某种类型的键盘的情况下就一头扎进去。我想这只是我的实际天性。我意识到这种比较是微弱的，因为当我制作 dactyl 时，我必须手工连接键盘矩阵。相比之下，组装麦角洐生是件轻而易举的事。我们今天的目标是展示我将如何使用这样的一个版本。

[![](img/4b9f77da9ad99775d9da0a214cd1f136.png)](https://hackaday.com/wp-content/uploads/2020/03/data-general-dasher.png)

Data General Dasher via [geekhack](https://geekhack.org/index.php?topic=98573.0)

你可以购买 ErgoDox 试剂盒，但我喜欢以自己奇怪的方式做事，为了更好地理解这一点，我想弄清楚所有的部分是什么，而不是把信息交给我。你也可以买这些已经组装好的键盘，但是这有什么意思呢？这样，我可以省下几乎所有的钱，自己做所有的工作！

当我这样做的时候，我试着把一切都考虑进去，这当然包括让它看起来尽可能的酷。我选择了透明的丙烯酸外壳，因为透明的电子产品确实是最好的电子产品。

当我订购带有蓝色阻焊膜的 PCB 时，第一个重要的美学决定就确定了。因此，请记住，电路板会透过外壳显示出来，我会在键帽上使用两种或三种蓝色配色，就像 Data General Dasher 终端上的键盘一样。

## 零件和人工

那么都是些什么*零件呢？可以想到的最有趣的是外壳选项、键帽、开关和电缆——一个用于连接电脑的迷你 USB 和一根 TRRS 音频电缆，这样两半就可以相互通话。但所有这些都只是锦上添花。在我们拿出糕点袋之前，让我们先打几个鸡蛋。*

### 多氯联苯(polychlorinated biphenyls)

ErgoDox 可以有 76 到 80 个键，区别在于拇指簇。你可以有八把普通大小的钥匙，或者像 Kinesis 一样有四把普通钥匙和两把双钥匙。

有一个左 PCB 和一个右 PCB，但设计是可以互换的，这意味着你需要两个相同的 PCB。你可以买一套已经做好的，或者买一套 gerbers，然后自己动手制作。我选择了第二个选项。我真的很想要紫色的 PCB，但是电路板又大又复杂，不划算，所以我尝试了一个新的板房。

[![](img/9044976e3926d4b76dec8d414685270b.png)](https://hackaday.com/wp-content/uploads/2020/04/ED-PCBs.png)

我可以从我得到外壳零件和所有电子元件的同一个地方订购 PCB，除了开关。但我觉得最好有备用板以防万一我把事情搞砸了。出于某种原因，我以为我会得到五套，因为它显示两个董事会时，我上传了压缩文件。没有。有五块电路板，相当于 2.5 个键盘。但我很确定，如果你将 Teensy 焊接到一边，I/O 扩展器焊接到另一边，那么一块板可以单独使用。如果是这样，请留意一篇关于大规模单手动马尔特龙式宏矩阵的帖子。嗯。

### 控制器和组件

ErgoDox 被设计为由运行开源固件的 Teensy 2.0 控制，如 [QMK](https://docs.qmk.fm/#/) 。我不确定一个更优秀的青少年是否会成功。我买了一套包括 Teensy 在内的组件——感觉比单独采购任何东西都便宜。76 个按键开关中的每一个都有一个 1N4148 二极管，ErgoDox PCBs 的设计允许通孔或 SMT 二极管。

由于 Teensy 没有接近 76 个 I/O 引脚，键盘使用 I/O 扩展芯片来建立行和列的矩阵。除此之外，还有一些无源器件，每一半一个 TRRS 插孔，一个迷你 USB 插孔，以及三个发光二极管，让你知道你正在哪个键盘层操作。

### 外壳和电缆

除了有趣之外，这款保护套在键盘设计和构造上也有所不同。这种键盘被设计成具有安装在板上的按键开关，这意味着在开关和 PCB 之间有一层 76 个按键开关形状的孔。这增加了开关的稳定性，并降低了焊接点的应力。你可以找到文件来剪切或打印你自己的案例层，很多人会卖给你预制的案例。

[![](img/ff29cc77c5e0eaa7bf88833aebf698c2.png)](https://hackaday.com/wp-content/uploads/2020/04/TRRS-kit.png) 我喜欢一些透明的电子产品，所以我的箱子是五层透明的丙烯酸树脂——顶部、底部、中间的按键开关板和中间的两个隔板。我唯一后悔的是没有进去把 ErgoDox 的商标改成除了漫画以外的任何东西，因为它会被看穿。

就像我说的，你需要一根 TRRS 线和一个迷你 USB。如果你购买零零碎碎的组件，你将需要第二个牺牲性的迷你 USB 来将微小的连接扩展到电路板的边缘。我买了一套组件，其中包括一个只需要电线和组装的 DIY 迷你 USB 连接器。

这是一种传统，有一个性感的 TRRS 电缆与降落伞套和一个匹配的 USB 电缆去配合它。预制电缆并不便宜，但是自制电缆还是很实惠的。我推迟订购 USB，直到我看到这个 paracord 与 PCB 的蓝色和我从键帽制造商订购的样品色卡一起看起来如何。

## ~~静音~~开关的声音！

<https://hackaday.com/wp-content/uploads/2020/04/outemu-blues.mp3?_=1>

[https://hackaday.com/wp-content/uploads/2020/04/outemu-blues.mp3](https://hackaday.com/wp-content/uploads/2020/04/outemu-blues.mp3)[![](img/1d2461768a11d8a5e654a606d0d330d3.png)](https://hackaday.com/wp-content/uploads/2020/04/bowl-of-cherries.jpg)

Maybe life really is just a bowl of Cherries.

捂住你的耳朵——开关将是樱桃 MX 蓝调。蓝调很吵，但没关系，因为在强制之前我就在家工作了。我考虑过买棕色的，因为那是 Kinesis 的颜色，我已经开始喜欢它们了，但是蓝色是如此的清脆悦耳。

棕色是触觉型的，而不是点击型的，它们需要的驱动力大约少 5 克左右，这对抗 RSI 的目的是有益的。但是由于我不会长时间使用这个键盘，我想蓝调应该没问题。

有那么一会儿，我想把所有的小指和无名指都换成棕色，其他地方都换成蓝色，但我有点担心键盘听起来会很奇怪，会让我失去打字的动力。但就像我说的，建造 ErgoDox 和随后的 Dactyl 的想法是有一个便携式的分离式 ergo 键盘，而不是巨大的 Kinesis，如果我这辈子有机会再做一次的话。Kinesis 声音大的部分原因是因为她的洞穴，回声情况。如果 ErgoDox 的声音大到足以打扰到人们，我可以在键帽的杆上放上小的消音 o 型圈。

[![](img/3dead0efdc34bfdc626e787b310d9e1c.png)](https://hackaday.com/wp-content/uploads/2020/04/DSA-ED-half.png)

Half a ‘Dox with a Fortnite-colored rainbow of DSAs. Image via [r/mk](https://www.reddit.com/r/MechanicalKeyboards/comments/609ml8/couldnt_find_the_cable_i_want_so_i_made_my_own/)

## 键帽

现在，我们来到了构建中最好、最有趣的部分。这也是最令人伤脑筋的决定，但没关系，因为键帽很容易改变。它们就像是你小伙伴的小外套，或者你喜欢的帽子。键盘布局编辑器是一个很好的尝试工具。

看起来很有趣，帽子也是建筑的一个功能部分。材料和风格可以决定键盘的用途，也可以决定它的用途，这取决于你想用它做什么。

### 奇妙的塑料

材料方面，主要有两种选择:ABS 和聚对苯二甲酸丁二醇酯(PBT)。我没必要告诉你什么是腹肌——总之，丹·马洛尼做得更好。PBT 是更厚、质量更高的塑料，手感很好。它能够承受紫外线而不变色，并且比 ABS 更能抵抗手指油产生的黏滑光泽。

PBT 键帽的侧面是光滑的，但顶部有一种令人愉快的粗糙感。PBT 键帽最糟糕的一点是，它们的颜色比 ABS 少得多。我还不知道 ErgoDox 会有什么样的键帽，但它们可能是蓝色或紫色的空白 PBT。

[![](img/4811206ad94a14feacdbf29d4607fa67.png)](https://hackaday.com/wp-content/uploads/2020/04/keycap-profiles.png)

Top row is DSA family, bottom row is SA. Images via [Signature Plastics](https://pimpmykeyboard.com/key-cap-family-specs/)

### 造型和侧写

选择键帽的另一个困难是决定键帽轮廓——这是指按键的形状和顶部的造型(或不造型)。如果你从短边看大多数标准的非 chiclet 键盘，你会发现键的顶部每行都有不同的形状。

为了减少手指移动的距离，像 F 键和数字键这样的上排的轮廓通常向下倾斜，ZXCVB 排向上倾斜，而空格键排是凸起的。家庭的第三排是最平坦的，尽管不是所有的家庭都有平坦的第三排。

我喜欢 SA 轮廓帽的外观，但它们超级高，可能会使我粗短的手指疲劳。我倾向于 DSA，因为我买了一些带有自动导向突起的运动，我喜欢它们的浅度。只要我得到所有的第 3 行，它们将被统一地描述，并且应该很容易转换回平面键盘。DSA 键帽也是 Kinesis 的一个很好的选择，所以如果他们在 ErgoDox 上没有工作，那么他们有一个地方可以去。

这可能是一个爱好的真正的金钱坑，如果你愿意的话，是一个大写 H 的爱好。我知道这样下去，我还是去了。希望我只做我会用的键盘，其余的回收利用。