# Hackaday 播客 115:人工智能在 Linux 终端不好，在 Python 中使用 Pico，3D 扫描不够

> 原文：<https://hackaday.com/2021/04/23/hackaday-podcast-115-ai-is-bad-at-linux-terminal-puppeting-pico-in-python-3d-scanning-comes-up-short/>

Hackaday 的编辑迈克·斯奇斯和埃利奥特·威廉姆斯拉开了为期一周的优秀黑客活动的帷幕。我们看到了 RGB LEDs 在无人机上作为数据通道的惊人用途，以及 IP 摄像机操作系统的秘密通过一些巧妙的逆向工程工具暴露无遗。有一个针对 Linux 终端的人工智能项目，它会猜测你实际想要运行的命令。在考虑了自动驾驶在航空航天业的发展程度之后，我们来看看在处理 3D 扫描对象模型时会发现哪些问题。

[//html5-player.libsyn.com/embed/episode/id/18834962/height/90/theme/custom/thumbnail/yes/direction/backward/render-playlist/no/custom-color/000000/](//html5-player.libsyn.com/embed/episode/id/18834962/height/90/theme/custom/thumbnail/yes/direction/backward/render-playlist/no/custom-color/000000/)

如果你想继续，看看下面的链接，一如既往，在评论中告诉我们你对这一集的看法！

[直接下载](https://traffic.libsyn.com/secure/hackaday/Hackaday_Podcast-Ep115.mp3)(约 60 MB)

### 关注 Hackaday 播客的地方:

*   [谷歌播客](https://podcasts.google.com/feed/aHR0cDovL2ZlZWRzLnNvdW5kY2xvdWQuY29tL3VzZXJzL3NvdW5kY2xvdWQ6dXNlcnM6OTM5MTM0NzIvc291bmRzLnJzcw)
*   [iTunes](https://itunes.apple.com/us/podcast/hackaday-podcast/id1447409683)
*   [Spotify](https://open.spotify.com/show/3NRV0mhZa8xeRT0EyLPaIp)
*   [装订机](https://www.stitcher.com/podcast/hackaday-podcast)
*   [RSS](http://hackaday.libsyn.com/rss)

## 第 115 集节目预告:

#### 本周新消息:

*   莱特的东西:首次火星动力飞行成功了
*   [乒乓球造就伟大的 PID 范例](https://hackaday.com/2019/07/31/ping-pong-ball-makes-great-pid-example/)
    *   [Mike 构建了一个 PID 平衡器，但需要重新考虑传感器](https://twitter.com/szczys/status/1383908555841933319)

#### 本周有趣的黑客:

*   [LED Hack 教 DJI Mini 2 无人机新招](https://hackaday.com/2021/04/20/led-hack-teaches-dji-mini-2-drone-new-tricks/)
*   [Camera Hack 剥离嵌入式 Linux 的层](https://hackaday.com/2021/04/20/camera-hack-peels-back-layers-of-embedded-linux/)
    *   [flashrom](https://www.flashrom.org/Flashrom)
    *   日津
*   [用 Pico 和 Python 搭建 PC 和嵌入式世界的桥梁](https://hackaday.com/2021/04/18/bridging-the-pc-and-embedded-worlds-with-pico-and-python/)
*   [AI 让 Linux 按你的意思做，而不是你说的做](https://hackaday.com/2021/04/20/ai-makes-linux-do-what-you-mean-not-what-you-say/)
    *   为机器人编写你自己的 Twitch 聊天控件——或者其他任何东西！
*   [可调活塞阻尼锤](https://hackaday.com/2021/04/19/adjustable-piston-damped-hammer/)
*   [74xx 扭曲的超外差接收机](https://hackaday.com/2021/04/19/a-superheterodyne-receiver-with-a-74xx-twist/)

#### 快速破解:

*   迈克的选择
    *   [一个假的 BBS 把软件安装到你的老式机器上](https://hackaday.com/2021/04/14/a-faux-bbs-gets-software-on-to-your-vintage-machines/)
    *   [洗涤剂 DRM 在小型洗碗机上落败](https://hackaday.com/2021/04/16/detergent-drm-defeated-on-diminutive-dishwasher/)
    *   [这款 ESP32 翻页机的节拍还在继续](https://hackaday.com/2021/04/16/the-beat-goes-on-with-this-esp32-page-turner/)
*   埃利奥特的选择
    *   引导加载程序上的毁灭是终极欺骗代码
    *   [厨房撞吧在点餐间玩毁灭战士](https://hackaday.com/2021/04/17/kitchen-bump-bar-plays-doom-between-orders/)
    *   [E.T .视频游戏在 10 行 BASIC 中被重新想象](https://hackaday.com/2021/04/17/e-t-video-game-gets-re-imagined-in-10-lines-of-basic/)
    *   [在 DEC 硬盘内](https://hackaday.com/2021/04/19/inside-a-dec-hard-drive/)

#### 不能错过的文章:

*   [船员龙的短距离跳跃开启了国际空间站代客泊车的时代](https://hackaday.com/2021/04/15/crew-dragons-short-hop-begins-the-era-of-valet-parking-at-the-iss/)
    *   [客机能自己降落吗？](https://www.flightdeckfriend.com/ask-a-pilot/can-a-plane-land-automatically)
    *   [它现在在做什么？](https://media.ccc.de/v/33c3-8033-what_s_it_doing_now) [航空事故中自动化依赖的作用](https://media.ccc.de/v/33c3-8033-what_s_it_doing_now)
*   [对 3D 扫描有什么期望，以及如何使用它](https://hackaday.com/2021/04/20/what-to-expect-from-3d-scanning-and-how-to-work-with-it/)