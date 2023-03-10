# 廉价、可扩展的落地钢琴全心全意地演奏

> 原文：<https://hackaday.com/2021/06/15/cheap-expandable-floor-piano-plays-with-heart-and-soul/>

自从我们看了电影《大人物》后，我们就一直想要一架落地钢琴。实际上，现在也是。我们有时想知道那部电影卖出了多少落地钢琴。它肯定也推出了一些构建，但可能没有一个像[这个由【Fred tsl】](https://www.instructables.com/Cheap-Expandable-Floor-Piano/)设计的丙烯酸和木质美人一样健壮。如果你想要更多的技术细节，[在 IO](https://hackaday.io/project/2295-cheap-expandable-floor-piano) 上查看这个项目。

最好的部分是，这架钢琴是模块化的，可以轻松地从 1 扩展到 8 个八度。每个八度音阶在一个 Arduino Mega 上运行，第一个八度音阶设置为主音阶，其他的设置为辅音阶。当[FredTSL]打开它时，主八度音阶会发送一条信息，找出有多少个八度音阶，然后给每个八度音阶分配一个数字。每当一个音符通过导电织物和传感器播放时，该程序都会获取键号和八度音程号，并将信息发送回主 Mega，主 Mega 通过 MIDI 音乐屏蔽播放该音符。

我们认为这看起来很棒，在上面跳舞非常有趣。请务必查看照片中的[构建日志，并在休息后逗留，因为你最好相信他们在这个宝贝上倾注了一些心血。毕竟，在这一点上，这几乎是强制性的。](https://photos.app.goo.gl/zgVPkDczEqyu9RbT6)

希望你可以建立一个落地式钢琴，但没有空间或木工技能？这是一个更小的无线版本，在 24 小时内完成。

 [https://www.youtube.com/embed/lHdwECdyA4Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lHdwECdyA4Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

