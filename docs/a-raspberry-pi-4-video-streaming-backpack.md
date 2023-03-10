# 一个树莓 Pi 4 视频流背包

> 原文：<https://hackaday.com/2019/09/27/a-raspberry-pi-4-video-streaming-backpack/>

你知道背包式直播视频系统的市场吗？它们的价格高达 1600 美元。显然，这些东西很受社交媒体巨头的欢迎，他们希望向坐在家中观看 YouTube 或 Twitch 的人展示自己精彩的生活。但是，相信即使像我们这样下巴松弛的乡巴佬也应该获得同样的技术，[Speedify Labs]一直在研究基于树莓 Pi 4 的更便宜的 DIY 替代方案。

现在你会注意到我们没有用“便宜”这个词来描述这个版本。正如这里所详述的，它仍然要花费你 600 美元左右。你总是可以用更便宜的版本替换索尼 AS-300 相机和 Elgato Cam Link 捕捉设备，但这个项目的目标是提供高质量的高清视频，可以与专业设备相媲美，因此避免了这种让步。

无论你的观众和预算对什么视频源感到满意，它最终都会被送入 Raspberry Pi 4，它使用`ffmpeg`一行程序对视频进行编码，并最终以 24 FPS 的速度推出 720p，这似乎是 Pi 所能做到的最好的。操作员可以使用 Circuit Playground Express 和 Python 脚本随意启动和停止流。

当然，所有这些的诀窍是通过可能不可靠的移动网络上传视频流。但正如你可能已经猜到的那样，这就是[Speedify Labs]开始展示其同名产品的地方:一种带有软件通道绑定的 VPN，它允许你将多个互联网连接结合起来，以获得更高的带宽和可靠性。通过他们的软件，Pi 能够通过 USB 连接的两部手机传输视频。正如下面的视频所展示的，即使当他们进出建筑物时，该设置也能够保持流。

我们自己的[Lewin Day]写了他在 Raspberry Pi 上用 4G 流媒体视频进行的实验，这可能会让任何想在旅途中观看他们节目的人感兴趣。不过，如果你想认真对待，那就值得看看【珍妮·李斯特】在丹麦 BornHack 2019 黑客营看到的[令人印象深刻的移动流媒体设备](https://hackaday.com/2019/08/18/an-all-in-one-conference-video-streaming-box/)。

 [https://www.youtube.com/embed/faL2J11xIgU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/faL2J11xIgU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

