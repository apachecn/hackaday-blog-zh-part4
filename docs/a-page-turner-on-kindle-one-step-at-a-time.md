# Kindle 上的翻页器——一步一个脚印

> 原文：<https://hackaday.com/2019/01/02/a-page-turner-on-kindle-one-step-at-a-time/>

你不必成为一个狂热的书虫，也能找到电子书阅读器的用处。以你当地的婚礼乐队为例:有大量的歌曲要唱，你不会真的想拖着装满和弦和歌词的文件夹到处走，无聊地浏览它们，为每首新歌找到正确的曲目。即使是最大的树尸爱好者也不能否认这里有一个电子书阅读器的舒适。由于翻页可以归结为简单地改变显示屏上的内容，你也不一定需要用手来完成。考虑到这一点，[mosivers]为他的音乐家兄弟的 Kindle 设计了一个 WiFi 脚踏开关，可以前后翻页。

越狱 Kindle 并安装 busybox 后，[mosivers]建立了一个 web 服务器，为两个 CGI 脚本提供服务，这两个脚本将之前记录的向前和向后翻转的输入事件分别写入到`/dev/input/event0`，本质上模拟了触摸屏按下的方式。作为对应的脚踏开关，装有一个电池供电的 ESP8266，作为 Kindle 连接的接入点，每当按下两个按钮中的一个时，就会请求那些翻页的 CGI 脚本。

如果你不喜欢在不用手的情况下破解你的设备来翻页，你当然可以考虑将[一个更机械的解决方案](https://hackaday.com/2018/08/15/a-remotely-controlled-kindle-page-turner/)与脚踏开关概念结合起来。如果你想看更多的[mosivers]，[可以看看我们之前报道过的他的 DIY 对话盒项目](https://hackaday.com/2018/06/14/diy-talkbox-gives-you-more-bounce-to-the-ounce/)。