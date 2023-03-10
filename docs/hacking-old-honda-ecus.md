# 黑掉旧的本田 ECU

> 原文：<https://hackaday.com/2021/07/03/hacking-old-honda-ecus/>

白天，汽车安全专家[P1kachu]在业余时间将自己的汽车作为业余爱好。他最近开始深入研究他在日本出行时使用的两辆老款本田汽车的发动机控制单元(ECU)。1996 年的 Integra 和 1993 年的 Civic 发动机相似，但 ECU 硬件不同。让事情变得更有趣；每个人都有一个调谐的 EPROM，公民的完全未知的来源。

[P1kachu]带着他的思域去商店更换 ECU 中烧坏的晶体管，与店主[Tuner-san]的一次偶然交谈让他踏上了旧 EPROMs 世界的旅程。[Tuner-san]拿出一个藏在柜台下的旧的 PROM 复制器，他小时候用它从 Famicom 等游戏机上复制 PROM 芯片。这些天来，他用它来维护他曾经工作过的汽车的旧 ECU 芯片的备份。这激起了[P1kachu]的好奇心，他想知道他是否能获得思域神秘舞会的内容。在尝试使用 PROM 复印机背面的串行端口失败后，他暴力破解了它。几分钟的谷歌搜索揭示了 27C256 EPROM 的 ASCII 引脚排列，他拿出一个 Arduino Mega 并将其连接到芯片上，然后开始运行。

![](img/85df8799929a7ae943e6a8002fcceb01.png)

Advantest R4945A EPROM Duplicator c.1980s

他目前正在钻研固件，使用 IDA 和他为三菱 M7700 系列 MCU 编写的[定制反汇编程序](https://github.com/P1kachu/oki-66207-processor)。他为此建立了一个 [GitHub 知识库](https://github.com/P1kachu/honda-p30-analysis)，并最终希望找出这个神秘的 ECU 芯片与工厂库存相比有哪些调整。他还想自己进行一点调整。随着[P1kachu]发布他的逆向工程成果，我们期待着更多的更新。我们还建议你像[P1kachu]一样，随身携带一个 Arduino、一块试验板和一些连接线——你永远不知道它们什么时候会派上用场。如果你对这些项目感兴趣，一定要看看[我们关于他 2018 年的老斯巴鲁黑客的文章](https://hackaday.com/2018/12/31/hacking-a-20-year-old-subaru/)。