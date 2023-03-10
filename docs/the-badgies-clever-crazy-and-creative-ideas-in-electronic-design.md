# Badgies:电子设计中的聪明、疯狂和创造性的想法

> 原文：<https://hackaday.com/2019/08/21/the-badgies-clever-crazy-and-creative-ideas-in-electronic-design/>

当你不得不围绕一系列约束进行设计时，工程创造力就变成了现实。只要有足够的时间、天赋和财富，我们几乎可以做任何事情，但是当你被限制束缚时，你能做什么呢？在设计会议徽章时，一些最具创意的电子制造技巧焕发了生机，因为制造多个徽章的能力、预算内的能力以及最重要的及时完成生产的能力都在发挥作用。

这种情况发生在全年和全球各地的会议上，但我见过的这些独特的艺术作品的最高浓度是在每年的 DEF CON 上。今年我喜欢看几十个有趣的项目，并在这篇文章中挑选了一些最酷的特性来展示。我仍然喜欢所有其他的，并有一个徽章 supercut 文章在路上，但在那之前，让我们看看钢筋混凝土汽车徽章，一种不同的 blinky bling，和其他一些辉煌的繁荣。

## 哦，不，他们没有:汽车黑客村徽章

![](img/011cbe9ad3b02f45429f97cc8632bc59.png)

DEF CON 27 上最疯狂的徽章无疑是汽车黑客村徽章。这是一辆功能性汽车，你可以通过蓝牙连接到它，然后开着它到处跑，让我们每个人都充满童趣。

是玩具车，那又怎样？这里的区别在于规模经济。如果你要运送 10，000 个，建造一个注射成型的外壳并容纳电子设备以无线控制它是没有问题的。但是这个项目只生产了 350 个 SUV 形状的徽章。在这种规模下，注射成型非常昂贵，尽管如此，他们还是努力向前。

外壳本身是激光切割和激光蚀刻的丙烯酸树脂，可以容纳一切。有一个 DC 电机使用蜗轮来驱动后轮。你可以在下面的视频中瞥见这一点。前轮的转向由一个非常小的业余爱好伺服机构负责，它使用一个丙烯酸杆。

抛开机械设计的壮举不谈，电子设备本身确实很聪明。在车辆的前部有一个承载巨大的恩智浦处理器的主 PCB，在靠近后部的地方有另一个用于电池管理的 PCB。两者由一对长而窄的 PCB 连接，PCB 与其他电路板呈 90 度角安装，电路板上带有照亮徽章的 RGB LEDs。在电路板以直角相交的地方，每个电路板上的焊盘排成一行，这样电路板就可以焊接在一起，携带一切正常工作所需的信号。背面有一个备用轮胎(也是丙烯酸的)，兼作旋转编码器，旁边有一个按钮。这是用户输入，反馈显示在组成挡风玻璃的有机发光二极管屏幕上。

 <https://hackaday.com/wp-content/uploads/2019/08/Car-Hacking-Village-Badge-DC27.mp4?_=1>

[https://hackaday.com/wp-content/uploads/2019/08/Car-Hacking-Village-Badge-DC27.mp4](https://hackaday.com/wp-content/uploads/2019/08/Car-Hacking-Village-Badge-DC27.mp4)

在肯定是一个艰苦的装配过程中，似乎到处都有痛点。我被告知手组装结束了大约 4 个小时每徽章网！这就是#Badgelife 的遗产，我想说，他们在 DC26 之后的第二天就开始了这项工作，硬件按时准备好了，让每个看到他们的人都很高兴。

## 少花钱多办事:太空力量

 [![Space-Force-badge-DC27](img/8511ab882a5a89585130999bef2bc628.png "Space-Force-badge-DC27")](https://hackaday.com/2019/08/21/the-badgies-clever-crazy-and-creative-ideas-in-electronic-design/space-force-badge-dc27/)  [![Space-Force-badge-DC27-rear](img/07f29788f3c01c666d13ebfe723bc363.png "Space-Force-badge-DC27-rear")](https://hackaday.com/2019/08/21/the-badgies-clever-crazy-and-creative-ideas-in-electronic-design/space-force-badge-dc27-rear/) 

乍一看，你可能想知道为什么我在今年的 Badgies 中加入了太空部队徽章。它做了徽章应该做的事情——挂在你的脖子上，闪烁，充当姓名标签。但是有很多精彩的细节让这个设计在很大程度上变得引人注目。这并不奇怪，因为威士忌海盗船员的[徽章已经](https://hackaday.com/2015/08/03/the-right-way-to-do-a-hacker-conference/)[传承了几年](https://hackaday.com/2015/08/10/all-the-unofficial-electronic-badges-of-def-con/)。

 [![Clever mounting of the OLED screen module](img/184035f865f245ee114831699cf63ed1.png "Space-Force-badge-DC27-screen-detail")](https://hackaday.com/2019/08/21/the-badgies-clever-crazy-and-creative-ideas-in-electronic-design/space-force-badge-dc27-screen-detail/) Clever mounting of the OLED screen module [![The front is perfectly flat and a masterclass of subtle design](img/01dac4f0936c290067894394d04bce60.png "Space-Force-badge-DC27")](https://hackaday.com/2019/08/21/the-badgies-clever-crazy-and-creative-ideas-in-electronic-design/space-force-badge-dc27-2/) The front is perfectly flat and a masterclass of subtle design [![Back of badge shows jumper wire and upside-down LEDs](img/cdd2c5ca8a943675866b122d49bde934.png "Space-Force-badge-DC27-no-battery")](https://hackaday.com/2019/08/21/the-badgies-clever-crazy-and-creative-ideas-in-electronic-design/space-force-badge-dc27-no-battery/) Back of badge shows jumper wire and upside-down LEDs

这个徽章的正面只有一个目的:让自己看起来惊艳。[True]竭尽全力确保顶层没有任何痕迹；它只需要一根跳线，而且这只是一个两层板！背光字母为 FR4，不含铜或阻焊膜，使用反向安装的普通 led。我焊接了这个，很难弥合焊盘和器件之间约 3 毫米的间隙。在这个过程中，我至少炸了四个。

OLED 模组的安装方式真的很工整。4 引脚接头被移除，这些走线直接焊接到徽章上的焊盘。另一方面，误用的直角表面安装接头充当机械紧固件。徽章上的孔正好适合玻璃屏幕作为边框。仔细看，你会发现还有一个红外收发器安装在电路板上。正面还有三个电容式触摸板，大部分肉眼看不见。

将徽章倒过来(如果你把它戴在脖子上，这是一个自然的手势)，加速度计会检测到它，并通过 ESP32 将其置于 WiFi AP 模式，以便你可以定制徽章上的名称。我是锂 18650 的忠实粉丝，它可以用徽章充电，但也可以在另一个项目中使用。相比之下，袋装电池从来没有其他用途。

## 让有光…和深度:SecKC 徽章

[![](img/25dde78b4bca0ff76564bb83f6adceab.png)](https://hackaday.com/wp-content/uploads/2019/08/SecKC-DC27-badge-wide.jpg)

这证明了你不需要多种颜色的发光二极管就能达到极致的闪亮效果。这个 [SecKC DC27 徽章](https://twitter.com/badgepirates)通过绿色发光二极管和负空间的组合做到了这一点。在预售量达到 90 枚左右后，该团队总共生产了 150 枚徽章。每个徽章包含 645(！)发光二极管。产量是一个问题，每个徽章都有一两个需要返工(向后放置等)，大约 50%的徽章需要更多的关注。

 [![Badge with top section removed](img/26b6c58baa7befe3315187503ca622fa.png "SecKC-DC27-badge-backplate-only")](https://hackaday.com/2019/08/21/the-badgies-clever-crazy-and-creative-ideas-in-electronic-design/seckc-dc27-badge-backplate-only/) Badge with top section removed [![Back of SecKC badge](img/a62c982f16aa3d82f5edc2e5ab2c9162.png "SecKC-DC27-badge-rear")](https://hackaday.com/2019/08/21/the-badgies-clever-crazy-and-creative-ideas-in-electronic-design/seckc-dc27-badge-rear/) Back of SecKC badge

让这个徽章看起来如此神奇的是使用了安装在三个连接器顶部的第二块电路板。在这里，您可以看到移除了剪影形电路板的较大 LED。这做了两件事:给你的眼睛一些深度，增加了比你想象的更多的兴趣，并在电路板之间提供了一个隐藏电池的地方。这些徽章由通过 Arduino IDE 编程的 ATmega328 驱动，并使用 EEPROM 存储动画模式。

## 小心你触摸的地方:弗兰肯斯坦徽章

[![](img/e4fa0a8182aaa2733558f3cfe047baba.png)](https://hackaday.com/wp-content/uploads/2019/08/FrankenBadge-DC27.jpg)

谢妮管，它们变得越来越稀有，它们很脆弱，你需要高电压来点亮它们。但是他们看起来很壮观，所以为什么不在他们周围建一个徽章呢！Frankenbadge 是 n0psl3d 博士的发明，他将数码管时钟的概念带入生活。

 [![High voltage behind a 3D-printed shell](img/a3732fcdd05a3e1153f5bd63dde42e09.png "FrankenBadge-DC27-rear")](https://hackaday.com/2019/08/21/the-badgies-clever-crazy-and-creative-ideas-in-electronic-design/frankenbadge-dc27-rear/) High voltage behind a 3D-printed shell [![Serial number, just paint segments you don't need black](img/55fe6fad0026d11ae054b389b15ed868.png "FrankenBadge-DC27-serial-number")](https://hackaday.com/2019/08/21/the-badgies-clever-crazy-and-creative-ideas-in-electronic-design/frankenbadge-dc27-serial-number/) Serial number, just paint segments you don’t need black

背面的高压位在某种程度上被安全地密封在 3D 打印的外壳内，或者被大量的热胶覆盖，并在丝网上警告不要靠近。徽章的序列号技术很有趣。三个 7 段数字已经用白色印在丝网上；把不需要的线段涂成黑色就行了。

令人惊讶的是，这是 n0psl3d 的第一个谢妮版本，他选择了 IN-12B 管。他带来了足够 50 个徽章的零件，但这是一个 DIY 徽章，组装取决于你。我唯一担心的是管子可能会掉出来。从你的蛋筒里掉冰淇淋会让你难过一天，但是从你的徽章里掉谢妮肯定会毁了你的黑客夏令营。

## 我们不需要建立徽章:DC503

 [![DC503-badge-DC27](img/464e0c20f491e1ebe9089bfc5fe45b4d.png "DC503-badge-DC27")](https://hackaday.com/2019/08/21/the-badgies-clever-crazy-and-creative-ideas-in-electronic-design/dc503-badge-dc27/)  [![DC503-badge-DC27-rear](img/8c0dac9f9f19387af04466f5faf8ccd9.png "DC503-badge-DC27-rear")](https://hackaday.com/2019/08/21/the-badgies-clever-crazy-and-creative-ideas-in-electronic-design/dc503-badge-dc27-rear/) 

徽章制作很难，尤其是有很多东西的时候，比如包括足够的按钮来制作一个完整的键盘。(我们为去年的超级徽章订购了大约 20，000 个瞬时开关，也参见上面提到的 SecKC 徽章产量。)这增加了复杂性，一路上的每一次颠簸都带来了一种威胁，即你可能无法及时完成生产。[DC 503 集团](https://twitter.com/dc503)通过简单地购买消费品并将其变成自己的产品，避开了今年所有的制造挑战。

[在过去的一年里，我们在 Hackaday 上多次介绍了 SMART Response XE。最初零售价为 100 美元，供每个学生在课堂上使用，你可以在二手市场上用几块骨头买到其中一个。它使用 ATmega186rf 并在 802.54 MHz 频带上通信。该团队重新利用徽章作为一个大聊天室。我最喜欢的是，他们能够钻穿通常被电池盖隐藏的外壳部分，以接触到用于刷新微控制器的焊盘。](https://hackaday.com/tag/smart-response-xe/)

## 还会有更多

去年，我花了所有时间在 DEF CON 上，试图找到每一个徽章制造商，看看他们在做什么。尽管今年我参加了更多的讲座，但我还是设法找到了 50 个左右的原创作品。Badgies 只是一个小集合，它在艺术形式上的创造性引起了我的注意。但其余的同样值得一看。请继续关注 Hackaday，在下一篇文章中休息一下！