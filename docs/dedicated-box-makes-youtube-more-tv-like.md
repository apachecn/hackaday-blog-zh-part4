# 专用盒子让 YouTube 更像电视

> 原文：<https://hackaday.com/2021/08/20/dedicated-box-makes-youtube-more-tv-like/>

[裸露电线]是 YouTube 的超级粉丝，消耗了大量内容。如果这听起来很熟悉，也许你也应该[建立一个专门的 YouTube 盒子](https://www.instructables.com/The-YouTube-Box/)。你可以按下按钮，那里有发光二极管，你可以从其他屏幕上停下来看一会儿这个屏幕。[Exposed Wire]想让观看他们最喜欢的创作者的最新视频变得更容易，但我们认为这也更有趣。

Rasberry Pi 4 inside 每五分钟检查一次新视频，在一个文本文件中跟踪创作者的视频总数，并进行比较。如果其中一个频道有新视频，相应的 LED 就会亮起，新视频的 URL 就会链接到该按钮。按下按钮，Raspi 打开浏览器，转到 URL，最大化视频，关闭 LED，并更新文本文件中的视频计数。

我们喜欢这里的建筑工作。在 PETG，1/4 英寸的中密度纤维板墙壁由 3D 打印的 L 型支架连接。起初，[Exposed Wire]将 led 和按钮安装到 PCB 上，但这真的很复杂，所以他们改为印刷面板。结合屏幕周围的支架，完成的构建看起来不错。休息后，请查看构建蒙太奇。

普通的 YouTube 视频不再适合你了？尝试在 LED 矩阵上以低分辨率观看它们。

 [https://www.youtube.com/embed/OahYTTfvSnw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OahYTTfvSnw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

