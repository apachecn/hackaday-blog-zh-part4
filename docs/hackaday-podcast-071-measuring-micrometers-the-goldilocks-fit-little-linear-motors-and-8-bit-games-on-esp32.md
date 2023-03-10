# Hackaday 播客 071:测量千分尺、金发女郎模型、小型线性马达和 ESP32 上的 8 位游戏

> 原文：<https://hackaday.com/2020/06/12/hackaday-podcast-071-measuring-micrometers-the-goldilocks-fit-little-linear-motors-and-8-bit-games-on-esp32/>

黑客日的编辑迈克·斯奇斯和埃利奥特·威廉姆斯·范经历了一个奇妙的黑客周。大多数激光切割机都试图变得更大，但有一个小小的展示了你想要在你的锦囊妙计中的异国情调的组件。说到技巧，这款 CNC 卷轴锯拥有我们从未见过的运动学——只需看看极坐标与笛卡尔坐标元素的舞蹈即可。几十年来，我们一直在滥用`printf()`,但是仅仅通过调用这个图灵完全函数就可以运行任意操作。我们用对低成本笔记本电脑和精确测量的赞美来结束这一周。

[//html5-player.libsyn.com/embed/episode/id/16571309/height/90/theme/custom/thumbnail/yes/direction/backward/render-playlist/no/custom-color/000000/](//html5-player.libsyn.com/embed/episode/id/16571309/height/90/theme/custom/thumbnail/yes/direction/backward/render-playlist/no/custom-color/000000/)

如果你想继续，看看下面的链接，一如既往，在评论中告诉我们你对这一集的看法！

[直接下载](https://traffic.libsyn.com/secure/hackaday/838456618-hackaday-ep071-measuring-micrometers-the-goldilocks-fit-little-linear-motors-and-8-bit-games-on-esp32.mp3) (60 MB 左右。)

Where to Follow Hackaday Podcast

### 关注 Hackaday 播客的地方:

*   [谷歌播客](https://podcasts.google.com/feed/aHR0cDovL2ZlZWRzLnNvdW5kY2xvdWQuY29tL3VzZXJzL3NvdW5kY2xvdWQ6dXNlcnM6OTM5MTM0NzIvc291bmRzLnJzcw)
*   [iTunes](https://itunes.apple.com/us/podcast/hackaday-podcast/id1447409683)
*   [Spotify](https://open.spotify.com/show/3NRV0mhZa8xeRT0EyLPaIp)
*   [装订机](https://www.stitcher.com/podcast/hackaday-podcast)
*   [RSS](http://hackaday.libsyn.com/rss)

## 第 071 集节目笔记:

#### 本周新消息:

*   [Lattice Semiconductor 在最新 Propel SDK 许可中瞄准比特流逆向工程](https://hackaday.com/2020/06/05/lattice-semiconductor-targets-bitstream-reverse-engineering-in-latest-propel-sdk-license/)
*   [格滴 EULA 条款禁止 FPGA 比特流逆向工程](https://hackaday.com/2020/06/06/lattice-drops-eula-clause-forbidding-fpga-bitstream-reverse-engineering/)

#### 本周有趣的黑客:

*   [微型激光切割机让微型步进机工作](https://hackaday.com/2020/06/03/tiny-laser-cutter-puts-micro-steppers-to-work/)
    *   直线电机:[步进电机直线丝杆滑块](https://www.aliexpress.com/item/4000033935971.html)
    *   SMT 金属 WiFi 天线: [PRO-OB-440](https://www.digikey.com/product-detail/en/proant-ab/PRO-OB-440/1532-1001-1-ND/4895684)
    *   直角表面安装紧固件: [SMTRA440-9-6ET](https://catalog.pemnet.com/item/right-angle-fastener-type-smtra/surface-mount-r-angle-fastener-unified/smtra440-9-6et)
    *   [燃烧者 Trogdor！](https://www.youtube.com/watch?v=90X5NJleYJQ)
*   [CNC 线锯首次切割前景看好](https://hackaday.com/2020/06/04/cnc-scroll-saw-makes-promising-first-cuts/)
*   [在 ESP32 上运行您最喜爱的 8 位游戏](https://hackaday.com/2020/06/09/run-your-favorite-8-bit-games-on-an-esp32/)
    *   有史以来最小的游戏机。永远不会。
    *   [参观可用的诺基亚液晶显示屏](https://hackaday.com/2010/10/14/touring-the-available-nokia-lcd-screens/)
*   [面向现代的开放式硬件调制解调器](https://hackaday.com/2020/06/09/an-open-hardware-modem-for-the-modern-era)
    *   建立您自己的拨号网络服务提供商——现在有了调制解调器池！
*   [在对 Printf()的单次调用中实现井字游戏](https://hackaday.com/2020/06/05/tic-tac-toe-implemented-in-single-call-to-printf/)
    *   [控制流弯曲:控制流完整性的有效性](https://www.usenix.org/system/files/conference/usenixsecurity15/sec15-paper-carlini.pdf) (PDF)
*   [用金发女孩方法(和 OpenSCAD)找到完美的零件匹配](https://hackaday.com/2020/06/09/finding-perfect-part-fits-with-the-goldilocks-approach-and-openscad/)
    *   [了解你的配合和公差](https://hackaday.com/2019/02/25/know-your-fits-and-tolerances/)

#### 快速破解:

*   迈克的选择:
    *   [行动摄像机的外部电池模块可实现非破坏性操作](https://hackaday.com/2020/06/09/external-battery-mod-for-action-camera-does-it-non-destructively/)
    *   [您的 ESP32 项目的迷你图](https://hackaday.com/2020/06/06/sparklines-for-your-esp32-projects/)
    *   [电路雕塑时钟走 Pew Pew](https://hackaday.com/2020/06/08/circuit-sculpture-clock-goes-pew-pew/)
*   埃利奥特的选择:
    *   [旋转控制器拨入电脑音量](https://hackaday.com/2020/06/04/rotary-controller-dials-in-pc-volume/)
    *   [为无线 GDB 行动的黑魔法添加 WiFi](https://hackaday.com/2020/06/04/adding-wifi-to-black-magic-for-wireless-gdb-action/)
    *   [他们是如何从 SN76489 8 位声音芯片中获得采样声音的？](https://hackaday.com/2020/06/05/how-did-they-get-sampled-sounds-from-an-sn76489-8-bit-sound-chip/)

#### 不能错过的文章:

*   [上网本:外形被时代遗忘](https://hackaday.com/2020/06/04/netbooks-the-form-factor-time-forgot/)
*   [手握活页簿](https://hackaday.com/2017/04/28/hands-on-with-the-pinebook/)
*   [游标卡尺和螺旋千分尺，不折不扣的测量](https://hackaday.com/2020/06/08/vernier-calipers-and-micrometer-screw-gauges-measuring-without-compromise/)