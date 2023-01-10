# 跟踪 Spotify 上的 Last.fm 流

> 原文：<https://hackaday.com/2019/03/11/stalking-last-fm-streams-on-spotify/>

早在社交媒体和 Web 2.0 的早期，Last.fm 是互联网上最重要的音乐网站之一。它拥有一个巨大的库，包含了有史以来每首歌曲的内容，还有一个推荐新歌的优秀算法，很快就获得了大量的追随者。不幸的是，它的商业模式和追随者这些年来发生了变化，但仍然有一个顽固的用户群。[Hexalyse]对 Spotify 的算法不满意，[因此开发了一个工具，让她能够实时跟踪 Last.fm 用户正在听的内容。](https://hexaly.se/2019/02/27/how-to-listen-along-a-last-fm-user-on-spotify/)

Last.fm 的主要特点是，它允许你告诉别人你在听什么，方法是在你播放时“搜索”你的曲目。可以通过 Last.fm API 从任何用户那里收集这些实时数据，从而使该项目成为可能。[Hexalyse]创建了一个 Python 脚本，通过 Last.fm 查询选定用户的当前播放曲目，然后将歌曲数据交给 Spotify API 在本地播放音乐。

这是一种寻找新音乐的有趣方式，依靠人类的品味而不是一堆数据中心代数。[【Hexalyse】已经将代码上传到 Github，如果你渴望亲自尝试的话](https://github.com/Hexalyse/LastFmListenAlong)。当然，如果你将它与 Macintosh SE/30 上的 [Spotify 整合，你会得到加分。](https://hackaday.com/2018/12/21/giving-an-old-mac-spotify/)