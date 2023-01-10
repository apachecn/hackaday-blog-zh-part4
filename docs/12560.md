# Hackaday 播客 152: 555 计时器盛会，EMF 芯片故障 3 路，磁性机械键盘，和有史以来最好的三录相机

> 原文：<https://hackaday.com/2022/01/21/hackaday-podcast-152-555-timer-extravaganza-emf-chip-glitching-3-ways-a-magnetic-mechanical-keyboard-and-the-best-tricorder-ever/>

加入 Hackaday 主编埃利奥特·威廉姆斯和执行主编汤姆·纳尔迪的行列，他们将带您了解本周的最佳故事和项目。对于观众中的物理媒体爱好者来说，有一些非常不幸的消息，但如果你对 50 岁的集成电路特别感兴趣，你会喜欢听到 555 定时器竞赛的获胜者。我们将看看一个由 ESP32 供电的唱歌电路雕塑，赞美 3D 印刷开关的优点，跟随一个黑客建造终极 *Star Trek* tricorder prop 的梦想，并尝试思考如何让电子设备屈服。坚持到最后，让我们仔细看看一些关于嗅出计算机病毒的非同寻常的说法，并通过思考为什么每个人都试图开车跑这么远来结束事情。

如果你想继续，看看下面的链接，一如既往，在评论中告诉我们你对这一集的看法！

[//html5-player.libsyn.com/embed/episode/id/21849125/height/90/theme/custom/thumbnail/yes/direction/backward/render-playlist/no/custom-color/000000/](//html5-player.libsyn.com/embed/episode/id/21849125/height/90/theme/custom/thumbnail/yes/direction/backward/render-playlist/no/custom-color/000000/)

[直接下载](https://traffic.libsyn.com/secure/hackaday/Hackaday_Podcast-Ep152.mp3) (65 MB)

Where to Follow Hackaday Podcast

### 关注 Hackaday 播客的地方:

*   [谷歌播客](https://podcasts.google.com/feed/aHR0cDovL2ZlZWRzLnNvdW5kY2xvdWQuY29tL3VzZXJzL3NvdW5kY2xvdWQ6dXNlcnM6OTM5MTM0NzIvc291bmRzLnJzcw)
*   [iTunes](https://itunes.apple.com/us/podcast/hackaday-podcast/id1447409683)
*   [Spotify](https://open.spotify.com/show/3NRV0mhZa8xeRT0EyLPaIp)
*   [装订机](https://www.stitcher.com/podcast/hackaday-podcast)
*   [RSS](http://hackaday.libsyn.com/rss)

## 第 152 集节目预告:

#### 本周新闻:

*   [SGX 的反对阻止了 4K 蓝光光盘在电脑上的播放](https://hackaday.com/2022/01/18/sgx-deprecation-prevents-pc-playback-of-4k-blu-ray-discs/)
*   祝贺 555 计时器比赛的获胜者！
    *   [巨型 555 定时器](https://hackaday.io/project/182863-giant-555-timer)
    *   [烛台 555](https://hackaday.io/project/182920-menorah555)
    *   [Cyclotone–机械朋克控制台音序器](https://hackaday.io/project/181880-cyclotone-the-mechanical-punk-console-sequencer)

#### 那是什么声音？

*   如果你知道本周的声音是什么，[填写这张表格就有机会赢得一件 Hackaday 播客 t 恤。](https://docs.google.com/forms/d/e/1FAIpQLSfdrclDxllgV_K-aJ4lFn4jCxXCWTVtbBqnCVMTR4OReVOu8A/viewform?usp=sf_link)

#### 本周有趣的黑客:

*   [Ioalieia 诡异的声音:一个 ESP32/Valve/Analog 混合电路雕塑](https://hackaday.com/2022/01/15/the-eerie-sounds-of-ioalieia-an-esp32-valve-analog-hybrid-circuit-sculpture/)
    *   [ESP32 是这个艺术装置背后的大脑](https://hackaday.com/2021/08/22/esp32-is-the-brains-behind-this-art-installation/)
*   [3D 打印磁性开关承诺真正的定制键盘](https://hackaday.com/2022/01/17/3d-printed-magnetic-switches-promise-truly-custom-keyboards/)
*   [巨型 3D 打印件](https://hackaday.com/2022/01/16/giant-3d-prints-piece-by-piece/)
*   [改进已经很惊人的*星际迷航*道具](https://hackaday.com/2022/01/14/improving-an-already-phenomenal-star-trek-prop/)
*   [用 PicoEMP 为你的逆向工程荣耀之路制造障碍](https://hackaday.com/2022/01/15/glitch-your-way-to-reverse-engineering-glory-with-the-picoemp/)
*   [以错误的方式做正确的事情:用 555 个定时器转储 STM8 固件](https://hackaday.com/2022/01/15/doing-the-right-thing-the-wrong-way-dumping-stm8-firmware-with-555-timers/)

#### 快速破解:

*   埃利奥特的选择:
    *   [AI 相机知道它的 S**t](https://hackaday.com/2022/01/17/ai-camera-knows-its-st/)
    *   [超便宜的 PCB 扳手是完美的套件配件](https://hackaday.com/2022/01/18/ultra-cheap-pcb-wrenches-make-perfect-kit-accessory/)
    *   [三板:钥匙短，文档长](https://hackaday.com/2022/01/18/threeboard-short-on-keys-long-on-documentation/)
*   汤姆的选择:
    *   [酸损 Game Boy 修复](https://hackaday.com/2022/01/17/acid-damaged-game-boy-restored/)
    *   [改进您的前面板](https://hackaday.com/2022/01/15/improve-your-front-panels/)
    *   [连载工作室一年](https://hackaday.com/2022/01/15/serial-studio-one-year-on/)

#### 不能错过的文章:

*   [通过嗅探恶意软件的 EM 签名来识别恶意软件](https://hackaday.com/2022/01/19/identifying-malware-by-sniffing-its-em-signature/)
*   [远程电动汽车即将问世](https://hackaday.com/2022/01/19/longer-range-evs-are-on-the-horizon/)