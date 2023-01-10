# Hackaday 播客 149:芭蕾舞机器人平衡，弯曲跟踪猫粮，PCB 在手术刀下，阿蒂尼做 555

> 原文：<https://hackaday.com/2021/12/17/hackaday-podcast-149-ballerina-bot-balances-flexures-track-cat-food-pcb-goes-under-the-knife-and-an-attiny-does-the-555/>

新任命的 Hackaday 主编埃利奥特·威廉姆斯和特约撰稿人丹·马洛尼站在播客麦克风后面，让你了解本周所有重要的黑客事件。我们将拥有 iPad 的鲍勃·罗斯时刻，为了避免订购 555 而不择手段，用烤面包机烤 Wii 游戏机。需要用逻辑芯片做一个 VGA 适配器？或者也许你想量化人类意识的内在深度？不管怎样，我们会保护你的。

[//html5-player.libsyn.com/embed/episode/id/21518549/height/90/theme/custom/thumbnail/yes/direction/backward/render-playlist/no/custom-color/000000/](//html5-player.libsyn.com/embed/episode/id/21518549/height/90/theme/custom/thumbnail/yes/direction/backward/render-playlist/no/custom-color/000000/)

如果你想继续，看看下面的链接，一如既往，在评论中告诉我们你对这一集的看法！

[直接下载](https://traffic.libsyn.com/secure/hackaday/Hackaday_Podcast-Ep149.mp3) (55 MB)

Where to Follow Hackaday Podcast

### 关注 Hackaday 播客的地方:

*   [谷歌播客](https://podcasts.google.com/feed/aHR0cDovL2ZlZWRzLnNvdW5kY2xvdWQuY29tL3VzZXJzL3NvdW5kY2xvdWQ6dXNlcnM6OTM5MTM0NzIvc291bmRzLnJzcw)
*   [iTunes](https://itunes.apple.com/us/podcast/hackaday-podcast/id1447409683)
*   [Spotify](https://open.spotify.com/show/3NRV0mhZa8xeRT0EyLPaIp)
*   [装订机](https://www.stitcher.com/podcast/hackaday-podcast)
*   [RSS](http://hackaday.libsyn.com/rss)

## 第 149 集节目预告:

#### 本周新闻:

*   向 Mike Szczys 深情告别:[今天是我在 Hackaday 的最后一天；感谢所有的黑客！](https://hackaday.com/2021/12/10/today-is-my-last-day-at-hackaday-thanks-for-all-the-hacks/)
*   log4j 漏洞的深远影响
    *   乔纳森·本内特在本周的安全中报道了[的细节](https://hackaday.com/?p=512070)
    *   [火星直升机是否受到 log4j bug 的威胁？](https://www.techradar.com/news/even-the-ingenuity-mars-helicopter-is-vulnerable-to-log4j)
*   急切地等待着 12 月 22 日詹姆斯·韦伯太空望远镜的发射
    *   [30 天的恐怖:发射 JWST 的后勤工作](https://hackaday.com/2021/11/02/30-days-of-terror-the-logistics-of-launching-the-james-webb-space-telescope/)

#### 那是什么声音？

*   一个新的声音难倒了一个新的搭档主持人！
*   如果你知道答案，[你可以赢得一件 t 恤](https://forms.gle/ZHiJ2YQAWrkX6M7E8)！

#### 本周有趣的黑客:

*   [一个自动扶正平衡机器人以简单的方式配置](https://hackaday.com/2021/12/13/a-self-righting-balancing-robot-configured-the-easy-way/)
    *   [我是科幻的化身；我是手柄](https://hackaday.com/2017/02/27/i-am-science-fiction-incarnate-i-am-handle/)
*   [用真实画笔在 IPad 上进行数字绘画](https://hackaday.com/2021/12/10/digital-painting-on-an-ipad-with-real-brushes/)
*   [PCB 显微外科将夹具放入板内](https://hackaday.com/2021/12/14/pcb-microsurgery-puts-the-bodges-inside-the-board/)
    *   [BOMU:有问题的部分](https://github.com/femtoduino/bomu-hardware/)
    *   [本周失败:黑客作家试图修复 Xbox】](https://hackaday.com/2021/12/08/fail-of-the-week-hackaday-writer-attempts-xbox-repair/)
*   你总是可以用 ATtiny 来代替 555
    *   [555 计时器大赛归来！](https://hackaday.com/2021/12/01/the-555-timer-contest-returns/)
    *   [555 使能微处理器](https://hackaday.io/project/182915-555enabled-microprocessor)
*   [难以置信的弯曲机制有助于重置猫日历](https://hackaday.com/2021/12/14/fabulous-flexure-mechanism-makes-for-resetting-cat-calendar/)
*   [满足您所有复古需求的超薄 7400 逻辑 VGA 板](https://hackaday.com/2021/12/14/a-slim-7400-logic-vga-board-for-all-your-retro-needs/)
    *   [低分辨率显卡仍然令人惊叹，因为它是由逻辑芯片制成的](https://hackaday.com/2019/07/07/low-res-video-card-is-still-amazing-since-its-made-out-of-logic-chips/)

#### 快速破解:

*   埃利奥特的选择
    *   Wii 在面包屑监狱里走到了尽头
    *   [谷歌的 T-Rex 游戏移植到 ESP32](https://hackaday.com/2021/12/15/googles-t-rex-game-ported-to-the-esp32/)
    *   [一种表达编程挫败感的编程语言](https://hackaday.com/2021/12/14/a-programming-language-to-express-programming-frustration/)
*   丹的选择
    *   [3D 打印在创纪录的时间内制造出“玻璃”眼睛](https://hackaday.com/2021/12/10/3d-printing-delivers-glass-eyes-in-record-time/)
    *   [如果操作得当，控制器更换可以节省硬盘空间](https://hackaday.com/2021/12/11/controller-swaps-can-save-an-hdd-if-you-do-it-right/)
    *   [100 MHz 和 200 美元的差分探头时钟](https://hackaday.com/2021/12/12/differential-probe-clocks-at-100mhz-and-200/)

#### 不能错过的文章:

*   [意识的真正科学(不是纸上谈兵的科学)](https://hackaday.com/2021/12/15/the-real-science-not-armchair-science-of-consciousness/)
    *   最快的神经冲动[约为 200 英里/小时](https://hypertextbook.com/facts/2002/DavidParizh.shtml)，所以从你的大脑到你的手指的最小潜伏期为 11 毫秒。然而，音乐家可以更精确地把握时间。
*   过时的家庭电影格式的诱惑