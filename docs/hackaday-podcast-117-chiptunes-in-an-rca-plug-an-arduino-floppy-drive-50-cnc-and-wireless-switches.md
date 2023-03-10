# Hackaday 播客 117:RCA 插头的芯片调谐、Arduino 软驱、50 美元的 CNC 和无线开关

> 原文：<https://hackaday.com/2021/05/07/hackaday-podcast-117-chiptunes-in-an-rca-plug-an-arduino-floppy-drive-50-cnc-and-wireless-switches/>

Hackaday 的编辑迈克·什奇斯和埃利奥特·威廉姆斯讨论了来自互联网的最新黑客攻击。3D 打印的线性轨道听起来不像是功能性数控机床的配方，但本周有一个真的让我们大吃一惊。RCA 插头内价值 0.03 美元的微控制器按程序产生的音乐让我们很高兴(智能柔性 PCB 可能是其中最酷的部分)。有一个有趣的技巧，通过在虚拟机中运行并回显到 WireShark 来逆向工程 Android 应用程序的蓝牙通信。我们来看看在佛罗里达群岛发生的转基因蚊子实验到底是怎么回事。

本周的新游戏是“那是什么声音？”。使用以下展示笔记上的表格链接发送您的答案，一名获胜者将获得一件播客 t 恤。

[//html5-player.libsyn.com/embed/episode/id/19018901/height/90/theme/custom/thumbnail/yes/direction/backward/render-playlist/no/custom-color/000000/](//html5-player.libsyn.com/embed/episode/id/19018901/height/90/theme/custom/thumbnail/yes/direction/backward/render-playlist/no/custom-color/000000/)

如果你想继续，看看下面的链接，一如既往，在评论中告诉我们你对这一集的看法！

[直接下载](https://traffic.libsyn.com/secure/hackaday/Hackaday_Podcast-Ep117.mp3)(约 55 MB)

### 关注 Hackaday 播客的地方:

*   [谷歌播客](https://podcasts.google.com/feed/aHR0cDovL2ZlZWRzLnNvdW5kY2xvdWQuY29tL3VzZXJzL3NvdW5kY2xvdWQ6dXNlcnM6OTM5MTM0NzIvc291bmRzLnJzcw)
*   [iTunes](https://itunes.apple.com/us/podcast/hackaday-podcast/id1447409683)
*   [Spotify](https://open.spotify.com/show/3NRV0mhZa8xeRT0EyLPaIp)
*   [装订机](https://www.stitcher.com/podcast/hackaday-podcast)
*   [RSS](http://hackaday.libsyn.com/rss)

## 第 117 集节目预告:

#### 那是什么声音？

告诉我们你对本周“那是什么声音？”。下周的节目中，我们将从正确答案中随机抽取一个名字，赢取限量版 Hackaday 播客 t 恤。(目前仅限于零，但我们会为您创建一个！)

#### 本周新消息:

*   [看下面！中国重型火箭将在几天内失控重返大气层](https://hackaday.com/2021/04/30/look-out-below-chinas-heavy-lift-rocket-due-for-uncontrolled-reentry-within-days/)
    *   [SpaceX 火箭碎片落在华盛顿州房主的财产上](https://www.foxnews.com/science/spacex-rocket-debris-lands-on-washington-state-homeowners-property)
    *   [SpaceX 火箭部件降落在印度尼西亚——猎鹰 9 号——jcs at-16](https://spaceflight101.com/falcon-9-jcsat-16/spacex-rocket-parts-rain-down-over-indonesia/)
    *   [Sylacauga(陨石)–维基百科](https://en.wikipedia.org/wiki/Sylacauga_(meteorite))

#### 本周有趣的黑客:

*   [RCA Plug 独自演奏 16 分钟的 Chiptune 乐曲](https://hackaday.com/2021/05/05/rca-plug-plays-sixteen-minute-chiptune-piece-all-by-itself/)
    *   [at tiny MIDI 插头合成器](https://hackaday.com/2016/03/30/the-attiny-midi-plug-synth/)
    *   [最小的 MIDI 合成器？](https://hackaday.com/2016/01/08/the-smallest-midi-synthesizer/)
*   [虚拟 Android 蓝牙嗅探器击败 Soundbar】](https://hackaday.com/2021/05/02/soundbar-bested-by-virtual-android-bluetooth-sniffer/)
*   [逆向工程自供电无线交换机](https://hackaday.com/2021/05/02/reverse-engineering-self-powered-wireless-switches/)
*   [带软驱的 Arduino】](https://hackaday.com/2021/04/30/an-arduino-with-a-floppy-drive/)
*   [I2C 纸带阅读机不是你所想的](https://hackaday.com/2021/05/03/i2c-paper-tape-reader-is-not-what-you-think/)
    *   什么会出错？I2C 版
*   [一台价值 50 美元的数控机床](https://hackaday.com/2021/04/29/a-50-cnc/)
    *   [垃圾桶数控机床制造](https://hackaday.com/2015/11/21/garbage-can-cnc-machine-build/)
    *   它是玩具吗？原型？是黑客！

#### 快速破解:

*   迈克的选择
    *   [灯具兼作秘密环绕声扬声器](https://hackaday.com/2021/04/28/lamps-double-as-secret-surround-sound-speakers/)
    *   [泳池温度监控器安抚幸运但沮丧的孩子们](https://hackaday.com/2021/05/02/pool-temperature-monitor-mollifies-fortunate-but-frustrated-children/)
    *   [ASCII 示意图](https://hackaday.com/2021/04/29/ascii-schematic-diagrams/)
*   埃利奥特的选择
    *   [碳化硅芯片可以见鬼去了](https://hackaday.com/2021/05/03/silicon-carbide-chips-can-go-to-hell/)
    *   [不用离开床就能感受到外面的温度](https://hackaday.com/2021/05/04/feel-what-the-temperature-is-like-outside-without-leaving-your-bed/)
    *   [5 月 4 日](https://hackaday.com/2021/05/04/enjoy-an-ascii-version-of-star-wars-in-the-palm-of-your-hand-for-may-the-4th/)在你的手掌上享受一个 ASCII 版本的星球大战
    *   [在 IPod Nano 3G 上存储更多音乐的宏伟目标](https://hackaday.com/2021/05/02/an-epic-quest-to-put-more-music-on-an-ipod-nano-3g/)

#### 不能错过的文章:

*   [转基因蚊子:用于疾病预防的生物黑客](https://hackaday.com/2021/05/03/genetically-modified-mosquitos-biohacking-for-disease-prevention/)
*   [太阳能驱蚊 2.0](https://hackaday.io/project/174575-solar-scare-mosquito-20)
*   [探索任天堂 3DS 家酿的世界](https://hackaday.com/2021/04/28/exploring-the-world-of-nintendo-3ds-homebrew/)