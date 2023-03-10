# 一个假的 BBS 会把软件安装到你的老式机器上

> 原文：<https://hackaday.com/2021/04/14/a-faux-bbs-gets-software-on-to-your-vintage-machines/>

回到调制解调器和电话线的黄金时代，公告牌系统，或 BBSes，是在自己家里舒适地寻找新软件的好方法。在过去的几十年里，随着互联网作为一种更加灵活的软件分发方式取而代之，大多数网站已经关闭。然而[equant]是一个通过文本界面浏览 warez 的爱好者，所以用一种今天有用的方式重新创造了这种体验。[结果是 RetroBridgeBBS。](https://github.com/equant/RetroBridgeBBS)

该软件运行在现代的个人电脑上，最好是运行 Python 3 并有串口的 Linux 电脑。然后，你可以用一根零调制解调器电缆通过串口连接你的老式电脑。在复古电脑上启动适当的终端软件，你会得到一个类似 BBS 的界面。从这里，您可以搜索选定的在线软件库，并下载您喜欢的软件。主机通过串行链路解析来自复古 PC 的请求，并混洗从互联网下载的请求文件。目前它主要是为 Macintosh 用户设置的，有一些有用的功能来避免下载错误版本的 StuffIt 档案——这是 90 年代的一个长期困扰。未来的计划包括扩展系统以适应更多的平台。

从技术上来说，这是一种时代错误，但是 T2 感觉这是一种在老式电脑上安装软件的正确方式。当您缺少合适的软盘硬件、硬盘仿真器或网卡时，这也是一个很好的方法——所有这些都很昂贵且供应不足。当然，也有其他的方法——[你可以用 ESP8266 做一些漂亮的事情，难道你不知道](https://hackaday.com/2017/06/17/bbsing-with-the-esp8266/#more-260818)！休息后的视频。

 [https://www.youtube.com/embed/VK541GMzuaE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VK541GMzuaE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

