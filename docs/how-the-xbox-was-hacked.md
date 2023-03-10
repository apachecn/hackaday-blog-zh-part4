# Xbox 是如何被黑的

> 原文：<https://hackaday.com/2018/11/19/how-the-xbox-was-hacked/>

千禧年:这个词在 1999 年之前很少有人使用，但似乎一夜之间它无处不在。千禧年之交渗透到流行文化的方方面面。像莫比这样的非传统流行歌星为主流电视频道提供电子音乐，而观众在看过《黑客帝国》*后思考电脑是否是真正的敌人。我们在焦虑和期待之间徘徊——普林斯预言的即将到来的千年虫会带来文明的终结——PS2 即将发布。*

索尼准备再次控制视频游戏机市场。他们已经卖出了比所有竞争对手加起来还要多的第一代 PlayStation 游戏机。他们对游戏玩家的巨大影响力意味着，在 PS2 上架之前，下一代游戏不会出现。在索尼宣布他们机器的技术规格后，[一个新的竞争对手](https://www.gamespot.com/articles/microsofts-console-threat-x-box/1100-2450236/)进入“主机大战”的谣言开始传播。新的竞争对手是微软，一家参与日本公司游戏的美国公司。


> *【微软】发动**战争**对抗索尼争夺* *客厅控制权。”*
> 
> ***——克里斯·莫里斯，CNN 特约撰稿人***

## 我知道邦妮芙

在世界末日失败近两年后，微软于 2001 年 11 月 15 日在北美推出了 Xbox。该控制台比之前的任何控制台都更像 PC，具有 8g 硬盘、英特尔奔腾 III CPU 和尖端的 DVD-ROM 驱动器。微软将他们的 Windows APIs 集合 DirectX 整合到他们的机器中，这也是控制台得名的原因。它的目的是向大众介绍家庭影院电脑。Xbox 可以玩游戏、播放音乐，购买了专有的红外遥控加密狗后，它还可以播放 DVD 电影。

发布后的一周，Xbox 用户收到了麻省理工学院学生安德鲁“邦尼”黄的提前圣诞礼物，他发表了自己摆弄游戏机的经历。他详细介绍了如何从主板上提取 TSOP 闪存芯片，以及对其中内容的见解。黄提取了 Xbox 的 BIOS 映像，并发布到互联网上供任何人下载。他简直是在玩火，因为就在帖子发布 12 小时后，他接到了一个来自微软代表的电话。他也发了那个。

<https://hackaday.com/wp-content/uploads/2018/11/bunnie-huang-gets-a-call-from-microsoft.mp3?_=1>

[https://hackaday.com/wp-content/uploads/2018/11/bunnie-huang-gets-a-call-from-microsoft.mp3](https://hackaday.com/wp-content/uploads/2018/11/bunnie-huang-gets-a-call-from-microsoft.mp3)Voicemail from Microsoft representative regarding Huang’s student webpage

有了这些众所周知的信息，第一个 Xbox modchip 于 2002 年 5 月上市销售。Xtender modchip 承诺绕过复制保护，打破区域锁定，并开放播放 DVD 的能力，而不需要那个愚蠢的 IR 加密狗。版权保护的承诺仅仅是一个承诺。当时没有办法备份 Xbox 游戏，当光盘插入 PC 时无法读取。结果，modchips 成了事实上播放从其他地区合法进口的方式。

如果你想深入了解 Xbox 黑客，或者硬件黑客，写黑客的人也写了这本书；看看[邦尼]的开创性工作“[黑掉 Xbox](https://hackaday.com/2013/03/12/hacking-the-xbox-released-for-free-in-honor-of-aaron-swartz/) ”。

## 用这个模式温柔地杀死他们

Xbox 在 PC 架构中有着深厚的根基。除了英特尔 x86 CPU 和 IDE 硬盘之外，还有闪存卡，玩家可以用它从游戏机上传输保存的游戏文件。让这些存储卡有趣的不是它们的存储容量，而是它们的引脚排列。数据线的布局奇怪地类似于 USB。以至于不需要天才就能想出如何修改 Xbox 控制器来支持使用 USB 拇指驱动器而不是存储卡。

![Xbox controller USB mod](img/639bf664a6044a5f16a0700212f40df9.png)

Modified Xbox controller with female USB adapter.

这个简单的 mod 为文件在 Xbox 和 PC 之间飞行铺平了道路。在游戏开发者打算让游戏中的物品可用之前，保存可以被重塑以解锁游戏中的物品，并且它们也可以作为更为狡猾的东西的入口。

诚然，没有游戏是完美的，但这尤其适用于 Xbox 独占 MechAssault。具有讽刺意味的是，微软游戏的保存文件为 Xbox 的加密硬盘提供了漏洞，允许在 Xbox 操作系统上安装整个 Linux 发行版。微软试图通过发布他们的第一轮在线游戏补丁来堵塞漏洞，但是大多数 Xbox 用户都是离线玩的。在其他几个游戏中也发现了类似的保存漏洞，被统称为 Xbox soft mods。

你的普通消费者永远不会去寻找一个 modchip 解决方案，因为用技术术语来说，烙铁是“又热又慢”的。然而，Xbox soft mod 更琐碎的特性降低了进入 hackerdom 的门槛。像 Lik-Sang 这样的 Modchip 经销商出售现成的 Xbox-to-USB 适配器作为“开发工具”，当它作为技术电视节目出现在有线电视上时，整个保存-利用-安装 Linux 的过程变得更加容易。

 [https://www.youtube.com/embed/Esf74hqf8Sw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Esf74hqf8Sw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



Linux 软件优化来得很快，因为所有这些机器都有完全相同的规格。大量自制软件在 Xbox 上找到了自己的家，从街机模拟器到网络浏览器，应有尽有。最受欢迎的自制作品之一是 Xbox Media Center (XBMC ),它致力于播放你可以扔在一块硅片上的每一种媒体编解码器。XBMC 充分利用了 Xbox 的宽带互联网功能，允许用户订阅音频/视频 RSS 源，并且在微软停止生产该游戏机多年后，它仍将接收更新。最大的讽刺是，微软最初让 Xbox 成为客厅里的 PC 的计划完全实现了……它只是运行 Linux。