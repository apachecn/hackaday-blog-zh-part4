# Hackaday 播客 127:惠普尔特里夹具，嗅你的胃收音机，万用表哼修复，和 C64 演示；没有 C64

> 原文：<https://hackaday.com/2021/07/16/hackaday-podcast-127-whippletree-clamps-sniffing-your-stomach-radio-multimeter-hum-fix-and-c64-demo-no-c64/>

Hackaday 的编辑迈克·斯奇斯和埃利奥特·威廉姆斯帮助你了解一周的神奇黑客活动。我们不记得在演示场景中看到过软驱，但是可以肯定的是，有一个 C64 演示是在计算机断开连接后执行的。什么原因导致工作台工具的测量不可靠？有时候一个糟糕的水晶选择会让 AC 毁了这个派对。我们将深入探讨 Audacity 开源项目所有权变更的传奇故事，并讨论发电机激励电路——特别是它们在启动电网规模的发电机时的作用。

[//html5-player.libsyn.com/embed/episode/id/19831988/height/90/theme/custom/thumbnail/yes/direction/backward/render-playlist/no/custom-color/000000/](//html5-player.libsyn.com/embed/episode/id/19831988/height/90/theme/custom/thumbnail/yes/direction/backward/render-playlist/no/custom-color/000000/)

如果你想继续，看看下面的链接，一如既往，在评论中告诉我们你对这一集的看法！

[直接下载](https://traffic.libsyn.com/secure/hackaday/Hackaday_Podcast-Ep127.mp3) (60 MB 左右。)

### 关注 Hackaday 播客的地方:

*   [谷歌播客](https://podcasts.google.com/feed/aHR0cDovL2ZlZWRzLnNvdW5kY2xvdWQuY29tL3VzZXJzL3NvdW5kY2xvdWQ6dXNlcnM6OTM5MTM0NzIvc291bmRzLnJzcw)
*   [iTunes](https://itunes.apple.com/us/podcast/hackaday-podcast/id1447409683)
*   [Spotify](https://open.spotify.com/show/3NRV0mhZa8xeRT0EyLPaIp)
*   [装订机](https://www.stitcher.com/podcast/hackaday-podcast)
*   [RSS](http://hackaday.libsyn.com/rss)

## 第 127 集节目预告:

#### 那是什么声音？

告诉我们你对本周“那是什么声音？”。下周的节目中，我们将从正确答案中随机抽取一个名字，赢取限量版 Hackaday 播客 t 恤。(有多有限？这将是第六次。)

#### 本周新消息:

*   [一个时代的终结:NTSC 终于在美国走向黑暗](https://hackaday.com/?p=486883)
    *   [来自@CarissaHolohan 的讨论 NTSC 关闭的帖子](https://twitter.com/CarissaHolohan/status/1415133765047889924?s=03)
*   [黑客日大奖在家工作挑战赛的最后一个周末](https://hackaday.com/?p=486668&preview=true&preview_id=486668)

#### 本周有趣的黑客:

*   [NFC 谁在门口](https://hackaday.com/2021/07/13/nfc-whos-at-the-door/)
    *   [PN532 数据表](https://www.nxp.com/docs/en/nxp/data-sheets/PN532_C1.pdf)
*   [分形虎钳紧紧夹住奇形怪状的物体](https://hackaday.com/2021/07/10/fractal-vise-holds-odd-shaped-objects-tight/)
    *   [惠普树(机制)–维基百科](https://en.wikipedia.org/wiki/Whippletree_(mechanism))
    *   [3D 打印分形虎钳——你不知道你需要的最酷的工具——YouTube](https://www.youtube.com/watch?v=eCfw9fd0mHg)
    *   [罕见的古董分形老虎钳【修复】–YouTube](https://www.youtube.com/watch?v=QBeOgGt_oWU)
*   [使用 RTL-SDR 调谐至医疗植入物](https://hackaday.com/2021/07/11/tuning-into-medical-implants-with-the-rtl-sdr/)
    *   [GitHub–mer Banan/RTL _ 433:对 ISM 频段(和其他频率)设备的无线电传输进行解码的程序](https://github.com/merbanan/rtl_433)
*   [修复 Owon XDM2041 台式万用表上的噪声测量值](https://hackaday.com/2021/07/14/fixing-noisy-measurements-on-an-owon-xdm2041-bench-multimeter/)
*   [Raspberry Pi 摄像机代替立体显微镜](https://hackaday.com/2021/07/09/raspberry-pi-cameras-stand-in-for-stereo-microscope/)
    *   [新零件日:Raspberry Pi 相机采用 1200 万像素&合适的镜头](https://hackaday.com/2020/05/01/new-part-day-raspberry-pi-camera-gets-serious-with-12-megapixels-proper-lenses/)
    *   [这款树莓派是一款立体相机，还有更多功能](https://hackaday.com/2018/12/30/this-raspberry-pi-is-a-stereo-camera-and-so-much-more/)
*   [C64 演示，无 C64](https://hackaday.com/2021/07/08/c64-demo-no-c64/)
    *   [6502 额外操作码](http://www.ffd2.com/fridge/docs/6502-NMOS.extra.opcodes)

#### 快速破解:

*   迈克的选择
    *   [快速肮脏解决方案粉丝的家庭自动化](https://hackaday.com/2021/07/09/a-home-automation-solution-for-fans-of-quick-and-dirty-solutions/)
    *   [retro tech atacular:电灯的秘密生活](https://hackaday.com/2021/07/13/retrotechtacular-the-secret-life-of-the-electric-light/)
    *   [Dial-a-SID 是一个光荣的 Chiptune 点唱机](https://hackaday.com/2021/07/08/dial-a-sid-is-a-glorious-chiptune-jukebox/)
*   埃利奥特的选择:
    *   [由氚电池供电的俄罗斯方块掌上电脑，最终](https://hackaday.com/2021/07/14/tetris-handheld-powered-by-tritium-cell-eventually/)
    *   [感应绘画利用光和热来完成](https://hackaday.com/2021/07/13/responsive-paintings-do-it-with-heat-and-light/)
    *   [人随车拖车](https://hackaday.com/2021/07/12/human-following-utility-trailer/)

#### 不能错过的文章:

*   [黑启动:电网如何重启](https://hackaday.com/?p=484504)
*   [缪斯集团继续对胆大妄为的音盲进行处理](https://hackaday.com/2021/07/13/muse-group-continues-tone-deaf-handling-of-audacity/)