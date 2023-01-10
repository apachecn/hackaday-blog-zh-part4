# Valve 卖软件，那么所有的硬件是怎么回事？

> 原文：<https://hackaday.com/2021/08/16/valve-sells-software-so-whats-with-all-the-hardware/>

Steam 品牌效应很强。Valve Corporation 已经将他们的第三方市场变成了数百万人购买电脑游戏的首选。今年早些时候，这项服务的并发用户已经超过了 2500 万，打破了历史记录，所以他们所做的一切显然是有效的。然而，随着所有这些软件的销售，上个月 Valve 发布了一款新的硬件，他们称之为 Steam Deck。

使用你喜欢的口语，“不要躺在你的荣誉上”或“曼巴心态”，这并不是说手持 PC 领域的竞争对手在吹嘘可笑的销售数字。他们的核心是销售电脑游戏。那么，为什么要冒险制造硬件呢？

> 每当我们告诉人们我们正在创建一个新的控制器时，(Valve)经常被人们问的第一件事就是，“为什么？”有很多好的双模拟手柄控制器……不幸的是，在 PC 领域，大多数游戏都不是为传统手柄设计的。
> Scott Dalton，GDC 2016 演示文稿

## 那些蒸汽是从哪里来的？

Valve 在硬件开发领域的首次商业尝试是以“蒸汽机器”品牌的形式出现的。Valve 在 2013 年与成熟的 PC 硬件制造商合作，为游戏 PC 构建创建一套通用的规范。这些规格相当于好、更好或最好。寻求简化 PC 游戏的三个选项，尽管有一个主要问题，SteamOS。Valve 定制了一个 Debian Linux 版本，使用的方法与 Ray 在《梦想的领域》中使用的方法相同，“如果你建造了它，(游戏)就会到来”。他们没有。十年后的大部分时间里，个人电脑游戏移植到 Linux 仍然是个例外，而不是规则。

![Steam Piston Promo Image from Xi](img/3d0c0323d597c8fa9c47b46af719f474.png)

The first of the ill-fated Steam Machines, the Valve Piston modular computer, reportedly could run Crysis.

几年后，Valve 有了 PC 游戏应该出现在电视上的想法。这个想法采用了蒸汽链路和蒸汽控制器的物理形式。当与适当的游戏 PC 配对时，这些设备将允许用户在家中的任何电视上远程玩他们的游戏库。如果 PC 和 Steam 链接都硬连线到以太网，体验通常会很好。如果只剩下 WiFi，那绝对是更糟糕的体验(因为每个人的 WiFi 都很糟糕)。虽然 Valve 的这种硬件巡回演出的遗产在 2019 年以 5 美元一个的价格清算库存的那一天[得到了总结](https://boingboing.net/2019/11/29/you-can-pick-up-a-steam-contro.html)。这就是为什么 Steam Link 现在只是一个 app。

Valve 早在 2012 年就开始研究虚拟现实技术，但在 2016 年选择与智能手机制造商 HTC 合作开发商用 VR 耳机。当时围绕 VR 的言论就好像糖精这个词上面加了额外的糖。当数虚拟摄影棚数量的人没有手指时，对虚拟现实的品味就会变酸。市场停滞不前。在那里学到的经验显然导致了 Valve 在几年后创建了自己的产品(Valve Index)，所以 Valve 在 VR 中的故事还有待书写。然而，最能说明问题的统计数据可能是[只有大约四分之一的连接到 Steam 的 VR 头戴设备是他们的](https://web.archive.org/web/20210805000540/https://store.steampowered.com/hwsurvey/)。

## 如果你手上有蒸汽怎么办？

![Steam Deck Switch Game Gear GameBoy Advance Stack](img/693822da7df8db9561044b28a7e5c513.png)

Here’s how the Steam Deck stacks up with past handhelds. Photo credit: Jan Ochoa

便携式游戏设备的概念已经得到验证。任天堂的掌机历史已经见证了超过 5 亿次服务，所以难怪 Valve 看到了自己掌机的机会。Steam Deck 是一个一英尺长的平板，带有四个核心 AMD Zen 2 APU，16 GB 的 DDR5 RAM，在一个 7 英寸 1280×800 IPS 显示器上，包裹着全套控制器按钮。所有这些只需 399 美元的入门价格。不喜欢什么？

首先，Steam Deck 搭载了基于 Arch Linux 的 SteamOS 3.0。在大多数情况下，开源软件是值得庆祝的，但是 Linux 上的游戏现实与其说是盛宴，不如说是饥荒。Valve 计划用他们的兼容性工具 Proton 来补救这种情况。这个软件通过 Wine 充当 Windows API 调用到可移植操作系统接口调用之间的转换层，Wine 是许多 Linux 用户都非常熟悉的另一个工具。这意味着 Valve 不再等待开发人员将原生移植到 Linux，就像人类语言翻译一样，有些愚蠢是可以预料的。Valve 之外的一个独立的[软件测试人员小组编制了一个关于 Proton 性能](https://www.protondb.com/)的数据库，结果不言自明。这比过去游戏在 Linux 上的表现要好很多，但现在还为时尚早。

通过让潜在客户知道他们可以在蒸汽甲板上安装一个替代操作系统，阀门已经清新地打开。多人游戏爱好者肯定会想占便宜。许多在 PUBG 和堡垒之夜等游戏后台运行的反作弊服务目前在 SteamOS 上无法运行。Windows 安装将解决这个问题，然而，虽然 Hackaday 的读者对创建可引导媒体并不陌生，但事实是大多数玩家将坚持默认设置。

根据作者的估计，Steam Deck 代表了 Valve 在设计自己的硬件方面的第三次重大突破。之前像蒸汽控制器这样的努力值得称赞，因为他们敢于“重新发明轮子”。Index VR 头戴式耳机设计被广泛认为是同类最佳设计。尽管没有注意到 Valve 和数字 3 之间的奇怪关系是一种疏忽。如果你需要这种现象的说服力，就去问戈登·弗里曼。

 [https://www.youtube.com/embed/BQLEW1c-69c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BQLEW1c-69c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



关于 Valve 软件历史的更多信息，请查看这篇关于该公司 VR 和 AR 原型的文章。

[主图像来源:[蒸汽甲板](https://www.steamdeck.com/)