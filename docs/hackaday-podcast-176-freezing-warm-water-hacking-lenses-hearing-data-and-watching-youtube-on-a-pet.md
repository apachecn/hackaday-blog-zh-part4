# 黑客日播客 176:冷冻温水，黑客镜头，听数据，在宠物上看 YouTube

> 原文：<https://hackaday.com/2022/07/08/hackaday-podcast-176-freezing-warm-water-hacking-lenses-hearing-data-and-watching-youtube-on-a-pet/>

又到了播客时间，本周主编埃利奥特·威廉姆斯和特约撰稿人丹·马洛尼一起回顾了这个星球上最好的黑客，以及一些来自 off 的。我们将发现如何最好地捕捉闪电，讨论在温暖的时候冷冻水或冰淇淋的好处，看看我们是否能发现 R2D2 在那些哔哔声和水滴中真正谈论的是什么。一旦我们解码，就可以知道汤姆·纳尔迪在第 174 集老板带着他的隐藏信息离开时在做什么，以及模拟编码的数字数据是如何在播客制作和出版链中存活下来的。但你肯定不能在 Commodore 宠物上看 YouTube 视频，对吧？事实证明，这不是问题，3D 打印也不是新耳朵。

埃利奥特《超级秘密掌握剧本》的肉？也可以用在你的视频上！

`ffmpeg -i $infile.wav -c:v copy -af loudnorm=I=-17:LRA=5:tp=-1.5 -ar 44100 $outfile.flac`

[//html5-player.libsyn.com/embed/episode/id/23686190/height/90/theme/custom/thumbnail/yes/direction/backward/render-playlist/no/custom-color/000000/](//html5-player.libsyn.com/embed/episode/id/23686190/height/90/theme/custom/thumbnail/yes/direction/backward/render-playlist/no/custom-color/000000/)

[直接下载](https://traffic.libsyn.com/secure/hackaday/Hackaday_Podcast-Ep176.mp3)，录到磁带上，在你的音箱上播放。

如果你想继续关注，请点击下面的链接，并一如既往地在评论中告诉我们你对这一集的看法！

Where to Follow Hackaday Podcast

### 关注 Hackaday 播客的地方:

*   [谷歌播客](https://podcasts.google.com/feed/aHR0cDovL2ZlZWRzLnNvdW5kY2xvdWQuY29tL3VzZXJzL3NvdW5kY2xvdWQ6dXNlcnM6OTM5MTM0NzIvc291bmRzLnJzcw)
*   [iTunes](https://itunes.apple.com/us/podcast/hackaday-podcast/id1447409683)
*   [Spotify](https://open.spotify.com/show/3NRV0mhZa8xeRT0EyLPaIp)
*   [装订机](https://www.stitcher.com/podcast/hackaday-podcast)
*   [RSS](http://hackaday.libsyn.com/rss)

## 第 176 集节目预告:

#### 新闻

*   [美国宇航局与其任性的顶点卫星](https://www.yahoo.com/news/nasa-reestablishes-communications-with-its-wayward-capstone-satellite-155435917.html)重新建立通信
*   [Cruise robotaxis 在旧金山的这条街道上堵塞了数小时的交通——TechCrunch](https://techcrunch.com/2022/06/30/cruise-robotaxis-blocked-traffic-for-hours-on-this-san-francisco-street)

#### 那是什么声音？

*   祝贺[Seth]和所有《银翼杀手》的粉丝们！
*   需要随机数吗？[RANDOM.ORG–整数生成器](https://www.random.org/integers/?num=1&min=1&max=40&col=5&base=10&format=html&rnd=new)

#### 本周有趣的黑客:

*   热水比冷水结冰快吗？关于姆彭巴效应的争论仍在继续
*   [将适马镜头转换为佳能镜头，包含数码功能](https://hackaday.com/2022/07/01/converting-a-sigma-lens-to-canon-digital-functionality-included/)
    *   [镜头:从引火物到智能手机和虚拟现实](https://hackaday.com/2022/06/28/lenses-from-fire-starters-to-smart-phones-and-vr/)
*   你以为你知道马里奥赛车是怎么工作的吗？
*   [计算机视觉从镜头中提取闪电](https://hackaday.com/2022/07/01/computer-vision-extracts-lightning-from-footage/)
    *   [从高清视频中提取雷击](https://hackaday.com/2015/05/11/extracting-lightning-strikes-from-hd-video/)
    *   [可居住的系外行星黑客聊天](https://hackaday.com/2020/01/13/habitable-exoplanets-hack-chat/)
*   [GGWave 唱你数据的歌](https://hackaday.com/2022/07/06/ggwave-sings-the-songs-of-your-data/)
*   [BlixTerm 为准将宠物带来全速 YouTube 视频](https://hackaday.com/2022/07/01/blixterm-brings-full-speed-youtube-video-to-the-commodore-pet/)

#### 快速破解:

*   埃利奥特的选择:
    *   [液晶屏幕窗户是今年夏天最热门的款式](https://hackaday.com/2022/06/30/lcd-screen-windows-are-this-summers-hottest-case-mod/)
    *   [UART 不行？Arduino CANSerial Can！](https://hackaday.com/2022/07/04/uart-cant-arduino-canserial-can/)
    *   [紧要关头双电源](https://hackaday.com/2022/07/02/dual-power-supply-in-a-pinch/)
*   丹的选择:
    *   [GPS 频率标准，用于计时必须正确的时间](https://hackaday.com/2022/06/29/a-gps-frequency-standard-for-when-the-timing-has-to-be-right/)
    *   [在没有试管测试仪的情况下测试试管](https://hackaday.com/2022/07/03/testing-a-tube-without-a-tube-tester/)
        *   [现代试管测试仪使用 Arduino](https://hackaday.com/2021/09/24/modern-tube-tester-uses-arduino/)
    *   [使用这款 20 世纪 70 年代风格的桌面通知程序，永远不会错过任何一封电子邮件](https://hackaday.com/2022/07/05/never-miss-an-email-with-this-1970s-style-desktop-notifier/)

#### 不能错过的文章:

*   [3D 打印软骨迎来定制身体部位的耳朵](https://hackaday.com/2022/06/29/3d-printed-ear-transplant-ushers-in-ear-a-of-custom-body-parts/)
*   [解开黑客日播客隐藏信息](https://hackaday.com/2022/07/01/unraveling-the-hackaday-podcast-hidden-message/)
    *   [如何从空间接收图片](https://hackaday.com/2017/02/13/how-to-receive-pictures-from-spaaace/)