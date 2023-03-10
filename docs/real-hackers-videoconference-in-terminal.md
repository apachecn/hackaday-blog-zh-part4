# 真实黑客终端视频会议

> 原文：<https://hackaday.com/2020/12/15/real-hackers-videoconference-in-terminal/>

在某个时候，我们中的许多人都试图看看我们的数字生活中有多少可以通过舒适的终端来访问。我们试过用 Alpine 收发电子邮件，用 W3M 浏览网页，甚至通过 telnet 观看了《星球大战》。但是，在我们今天所处的日益远离社会的世界中，我们发现自己在问:视频通话怎么样？

好吧，我们不是问这个。但值得庆幸的是，安迪·孔(Andy Kong)和他的一个朋友创建了一款“安全的、基于文本的视频会议应用，可以从你的终端安全地访问”的 AsciiZOOM，他认为实现这一点是合适的。

你可能已经猜到了，[安迪]的解决方案用实时动画 [ASCII 艺术](https://hackaday.com/2020/01/09/vintage-mini-inkjet-prints-on-demand-ascii-art/)取代了我们都习惯的传统视频流。该系统的工作原理是从网络摄像头捕捉视频流，通过将其转换为 ASCII 字符来“压缩”每个像素，并将整个帧填充到 TCP 包中。每个客户端都连接到一个服务器(会议室？)来协调数据包，适当地来回发送它们。

虽然令人印象深刻但不切实际，这个项目唯一缺乏的地方是音频。[安迪]建议使用不和谐来解决这个问题，但这里希望我们能在版本 2 中看到字幕！AsciiZOOM 会很快取代我们最喜欢的视频会议套件吗？不。我们庆幸它的存在吗？你打赌。

 [https://www.youtube.com/embed/g4YCxM5STj0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/g4YCxM5STj0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

