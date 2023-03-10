# python 网络代理说服 sonos 流式传输 youtube

> 原文：<https://hackaday.com/2022/02/04/python-web-proxy-convinces-sonos-to-stream-youtube/>

(莫里斯-米歇尔·迪德洛)拥有一款 Sonos 智能音箱，他哀叹这款设备在不使用订阅服务的情况下，无法(或者根本不愿意)播放在线音乐。YouTube 音乐可以工作，但是作为一个订阅产品是有月费的，这很糟糕，因为你可以在 YouTube 上免费听很多内容。[Maurice]决定，前进的道路是深入研究 Sonos 固件如何访问“网络电台”资源，并看看是否可以利用这一点通过某种即时流转换过程从 YouTube 流式传输音频。

[![](img/e13f992c99981e516b08204c012ab0e6.png)](https://hackaday.com/wp-content/uploads/2022/02/1_Zdi_Oudq_Y3_Nhe_H8_Kua_PU_3g_734c8074dd.png)

What? No MP4 support for web radio? Curses!

所以让我们深入了解一下[莫里斯]是如何选择这种方法的。智能扬声器可以配置为添加各种流式音频源，并允许您添加自定义源。Sonos 固件支持除 MP3 之外的各种音频编解码器，但 YouTube 使用 MP4 格式。Sonos 不能处理来自 web 广播源的消息，所以除了定制转换器之外还能做什么呢？

经过一番挖掘，确定 Sonos 支持 [AAC 编码](https://en.wikipedia.org/wiki/Advanced_Audio_Coding)(这是 MP4 编码音频的方式)，但需要将其包装在 ADTS(音频数据传输流 *)* 容器中。通过使用 Flask 在 python 中构建一个反向 web 代理应用程序，可以很简单地从 web radio 请求中获取 YouTube 视频 ID，使用修改后的 [pytube](https://pypi.org/project/pytube/6.4.2/) 版本将请求转发到 YouTube，该版本被调整为不下载视频，而是播放视频。Pytube 使 Maurice 能够从 MP4 容器中提取 AAC 音频“原子”,然后用 ADTS 将它们打包并转发到 Sonos 设备上，Sonos 设备很高兴地认为这只是一个普通的旧 MP3 广播流，即使它不是。

[![](img/441d410238104f565ab5d631a58f2322.png)](https://hackaday.com/wp-content/uploads/2022/02/1_9g6_VA_0_JU_Fe_C_Ly6xh_ka_XBQ_954b46d68a.png)

可以说，Sonos [并没有最好的名声](https://hackaday.com/2020/02/24/ethics-whiplash-as-sonos-tries-every-possible-wrong-way-to-handle-iot-right/)，但是你不能否认里面有一些非常巧妙的技术。这是我们去年报道的一次巧妙的黑客攻击，给一个老学校的扬声器增加了 [Sonos 支持，以及一次漂亮的](https://hackaday.com/2021/05/15/using-ikea-guts-to-add-sonos-compatibility-to-a-vintage-speaker/)[拆除宜家 Sonos 兼容单元](https://hackaday.com/2019/10/11/tearing-down-ikeas-sonos-speaker/)，它使用了一些巧妙的设计技巧。

感谢[mip]的提示！

查尔斯·德鲁维奥在 Unsplash 上的专题图片。