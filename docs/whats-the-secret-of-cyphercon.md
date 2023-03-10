# 赛弗肯的秘密是什么？

> 原文：<https://hackaday.com/2019/04/21/whats-the-secret-of-cyphercon/>

塞弗肯并不特别大，也不在世界上迷人的地方——事实上，大多数从外地来的人都不得不与雪搏斗才能到达那里。然而，当我上周四走进这个骗局时，毫无疑问，一些令人敬畏的事情正在发生。人们三五成群地扎营，在电脑上疯狂地工作，谈话中挤满了在问答环节活跃起来的人&，无论你走到哪里，你都会发现人们在和新老朋友深入交谈。如果您错过了 Cyphercon 4.0，那么您需要为 5.0 做出努力。

休息之后，请和我一起关注这个位于密尔沃基市中心的为期两天的安全会议的精彩部分。

## 抓住骗局

 [![Team trying to make tape from transparency](img/55359a412a76e5ac49c1ff0adee4d7ed.png "cyphercon-transparency-laser-printer")](https://hackaday.com/2019/04/21/whats-the-secret-of-cyphercon/cyphercon-transparency-laser-printer/) Team trying to make tape from transparency [![Tape mock-up ready for printing](img/f6f2a007685addea1e6ecc8185f399ca.png "cyphercon-transparency-software")](https://hackaday.com/2019/04/21/whats-the-secret-of-cyphercon/cyphercon-transparency-software/) Tape mock-up ready for printing [![Cyphercon 4.0 badge reading paper tap](img/4772189ee26d056a213877753a8d3660.png "cyphercon-badge-2019-tape-reader-thumb")](https://hackaday.com/2019/04/12/cyphercon-badge-has-a-paper-tape-reader-built-in/cyphercon-badge-2019-tape-reader-thumb/) Cyphercon 4.0 badge reading paper tap

有很多人在努力捕捉旗帜。这是一个大会范围的挑战，展示谜题——有些是印刷的，有些是数字的，有些像物联网村鼓励硬件黑客——在那里你找到一个散列并将它们输入到记分牌中，为你的团队赢得分数。我采访了特伦顿·艾维，他组织了这次 CTF 和[，他为 Hackaday 播客](https://hackaday.com/2019/04/19/hackaday-podcast-ep-015-going-low-frequency-robotic-machines-disk-usage-for-budgets-and-cellphones-versus-weather/)分享了抓捕罪犯的故事。

上面的三位先生想出了一个绝妙的主意。正如我上周所写的，Cyphercon 徽章包括一个纸带阅读器。你可以解锁徽章的一部分，并通过运行磁带获得标志，但你可以让徽章表产生多少磁带是有限的。这三个人带了激光打印机和透明胶片。由于阅读器是红外的，他们打印了黑色的条纹，上面有空的点作为“洞”，并通过徽章进行了测试，但效果有限。

 [![Cypher Village starter puzzle](img/3c52e81336d7ef9b28dbcd8c57116c92.png "cypher-village-starter-puzzle")](https://hackaday.com/2019/04/21/whats-the-secret-of-cyphercon/cypher-village-starter-puzzle/) Cypher Village starter puzzle [![Graphics coming together](img/d0c924daad95c7fc73e0561d83c19b5f.png "cyper-village-card-puzzle")](https://hackaday.com/2019/04/21/whats-the-secret-of-cyphercon/cyper-village-card-puzzle/) Graphics coming together [![Card decks](img/d528c5c79f46dbfc6292b0d32af6c29f.png "cyper-village-multiple-cards")](https://hackaday.com/2019/04/21/whats-the-secret-of-cyphercon/cyper-village-multiple-cards/) Card decks

有很多人在破解磁带代码，并要求他们能找到的每个人扫描他们在注册时收到的二维码(快速获得 5 分)。tons 正在进行的另一项活动是 Cypher Village 挑战赛。你拿起一张明信片，上面有起始密码。一旦你拿到了，你就可以回去拿一副牌。这些卡片是一个视觉难题，但你需要不止一套来完成它，并开始发现和解决其中的难题。

## 你可能会学到很多东西

我越来越多地看到硬件黑客在安全会议上找到一席之地。我马上发现自己在硬件黑客村，今年它有自己简单的徽章。这里有一个钩子，如果你参加了教授如何转储固件和从拆卸中学习东西的研讨会，你就可以获得一个徽章。整洁！

 [![cyphercon-embeddedproject-front](img/7748c99fbd386de648457b7df32ff0ad.png "cyphercon-embeddedproject-front")](https://hackaday.com/2019/04/21/whats-the-secret-of-cyphercon/cyphercon-embeddedproject-front/)  [![cyphercon-embeddedproject-back](img/8390f28b5b49f430bf07a2b417348ea9.png "cyphercon-embeddedproject-back")](https://hackaday.com/2019/04/21/whats-the-secret-of-cyphercon/cyphercon-embeddedproject-back/) 

它组装起来有点像唱针。有一根跳线，一端焊接在电路板上。另一端用于接触 PCB 上的焊盘，以产生不同的行为。使用 ATtiny85、四个 led、一个电阻和一个 CR2032 纽扣电池支架，BOM 成本很低，并且所有这些都是在一个未经修改的煎锅上组装的。

[![](img/b4dadad9bcc1d844db34a3095d65bcb6.png)](https://hackaday.com/wp-content/uploads/2019/04/cyphercon-red-badge-safe-cracking.jpg) 我也给黑客 101 表试了一下。这是为了帮助人们快速掌握基本的黑客工具。现场有几名工作人员和几台电脑。我用 wire shark 介绍了数据包嗅探。

看看开锁村里展出了什么。大多数活动都有牌桌，你可以在那里学习开锁。我不习惯看到的一个很酷的东西是保险箱的多重锁。其中大多数只是没有外壳的表盘组件，但这个丙烯酸外壳很特别。里面是一个红色徽章——任何能打开保险箱的人都可以终身进入 Cyphercon。~~今年没落下，下一年好好温习一下技能吧。~~看起来它确实在 ng 闭幕式前 5 分钟被破解了！

## 谈话、艺术和徽章修复

我描述的已经很多了，但是整个周末还有三场讲座。冲突的日程安排意味着我不能看到所有我想看的东西，但是有两个我非常喜欢。

Michelle Meas 发表了一篇关于未来基因组数据库泄露会产生什么影响的演讲。你知道，那些人们作为礼物赠送的工具包，用你的 DNA 告诉你你来自哪里？我没有想到的是，你的 DNA 标记与第三代表亲和近亲有多接近。如果他们向其中一家公司提交了 DNA，即使你从未参加过任何一项测试，也有可能根据他们的结果推断出你的很多信息。

[艾瑞克·埃斯科巴和马特·奥姆](https://cyphercon.com/cyphercon-4-0/presentations/remote-wireless-pentesting-in-a-nutshell-or-ammo-can/)介绍了远程无线测试。他们对硬件的概述很有趣——包括评论说，如果你带着笔记本电脑到处跑，打开嗅探网络，人们会很好奇，但如果你在智能手机上这样做，没人会在意。他们也有一些关于用手机连接的测试设备邮寄包裹的故事…那不仅仅是你桌子上的联邦快递盒子。

 [![Large backdrop, about 7 feet tall by 10 feet wide](img/07abd64fddad7b3158bae4041a5b2ca2.png "cyphercon-great-art")](https://hackaday.com/2019/04/21/whats-the-secret-of-cyphercon/cyphercon-great-art/) Large backdrop, about 7 feet tall by 10 feet wide [![cyphercon-tall-art](img/ce95f92d2a5938049957533554836799.png "cyphercon-tall-art")](https://hackaday.com/2019/04/21/whats-the-secret-of-cyphercon/cyphercon-tall-art/)  [![Wire Engineer at his badge repair station](img/adcd055ba63bf8437b312b0f0540a44b.png "cyphercon-wire-engineer-badge-repair")](https://hackaday.com/2019/04/21/whats-the-secret-of-cyphercon/cyphercon-wire-engineer-badge-repair/) Wire Engineer at his badge repair station

我真的很喜欢看塞弗肯艺术展览。这里展示的大块作品是 Mar Williams 的作品。本文顶部的艺术作品来自会议程序，是[布莱恩“科因”范·斯特杜姆](https://twitter.com/KoynArtist)的作品。我还想对[的电线工程师](https://twitter.com/wireengineer)大声欢呼，他像冠军一样，整个会议都在修理损坏的徽章。是的，我在写关于徽章的文章时弄坏了我的，他马上就修好了。

## 不算大骗局的秘密

那么赛弗肯的秘密是什么呢？很特别。像所有较小的会议一样，它有着本次会议独有的传统和紧密的友谊。它很受欢迎，很有趣，而且它位于这个国家的一部分，那里的人们渴望更愉快的黑客挑战。