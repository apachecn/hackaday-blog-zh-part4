# 微软发布了你 30 年前就想要的源代码

> 原文：<https://hackaday.com/2020/05/22/microsoft-releases-the-source-code-you-wanted-almost-30-years-ago/>

在 20 世纪 70 年代末和 80 年代初，如果你有一台个人电脑，它很有可能要么启动到微软 Basic 的某个版本，要么你可以加载并运行 Basic。当然，还有其他版本，特别是针对非常小的计算机，但家用计算机 Basic 的黄金标准是微软的版本，当时称为 GW-Basic。现在你可以直接从微软获得曾经梦寐以求的微软 8086/8088 Basic 源代码，就像你在 1983 年发现它时一样。他们在[建立了一个只读的 GW-BASIC 库](https://github.com/microsoft/GW-BASIC)，大概是为了阻止对 GPU 加速的大量功能请求。

你可能想知道他们为什么要这么做？这当然是有教育意义的，尤其是如果你对汇编语言感兴趣的话。出于历史原因，你可能想得到一个副本，你也可以修改，为您最新的 retrocomputer 项目。

有一些有趣的花絮。有些源代码标明是翻译过来的。显然，微软对一些处理器有一个主实现——真实的或想象的——并可以从该代码翻译成 8088、Z-80、6502 或任何其他他们想要的目标处理器。

据我们所知，GW-Basic 与 IBM 的 BASICA 相同，但不需要某些 IBM PC ROMs 来运行。当然，BASICA 本身来自微软的 CP/M 语言 MBASIC，它起源于 Altair Basic。影响个人电脑多年的悠久历史。另外，关于 GW 代表什么还有争议。Gee-Whiz 是一个受欢迎的投票，但它可能代表“盖茨，威廉”，格雷格·惠顿(微软早期员工)，或盖茨-惠顿。源代码似乎没有回答这个问题。

不过，我们确实喜欢 1975 年的版权信息:

```
ORIGINALLY WRITTEN ON THE PDP-10 FROM
FEBRUARY 9 TO APRIL 9 1975

BILL GATES WROTE A LOT OF STUFF.
PAUL ALLEN WROTE A LOT OF OTHER STUFF AND FAST CODE.
MONTE DAVIDOFF WROTE THE MATH PACKAGE (F4I.MAC).

```

不久前微软发布了一些[旧版本的 MSDOS](https://hackaday.com/2018/10/01/microsoft-releases-crown-jewels-from-1982/) 。如果你有写一些 Basic 的冲动，你可能会放弃 GW-Basic，转而尝试 [QB64](https://hackaday.com/2018/02/22/quickbasic-lives-on-with-qb64/) 。

GW-基本盘和手动照片由【Palatinatian】[CC-SA-4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.en)。