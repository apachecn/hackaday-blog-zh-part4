# 苹果最好的电脑有无线网络

> 原文：<https://hackaday.com/2018/09/26/apples-best-computer-gets-wifi/>

苹果有史以来最伟大的电脑不是 Apple II，不是 Bondi Blue iMac，不是垃圾桶，当然也不是他们现在推出的过热的垃圾。苹果公司有史以来制造的最好的计算机是 SE/30，30 年前，它是一个微型便携式外壳的服务器，能够支持 128 兆内存。

多年来，人们已经将 SE/30 扩展到了绝对荒谬的程度，但现在我们有了一种简单的方法来为这款经典电脑添加 WiFi。[在 68kmla 论坛上](https://68kmla.org/forums/index.php?/topic/31078-adding-wi-fi-to-my-mac-se30/),【蚂蚁】发现了一种微型廉价卡，可以轻松充当以太网到 WiFi 的桥梁。在将这个卡连接到 Danaport 以太网卡上并弯曲一些铝作为支架后，他们有了一个从 30 年前的电脑背面伸出来的 WiFi 天线。

但是给旧电脑添加 WiFi 卡并不是什么新鲜事——这本来可以用 Pi 来完成，或者如果你是一个黑客，用 OpenWRT 来更新 TP-Link 路由器。要真正做到这一点，您需要与操作系统集成，这就是这个构建偏离轨道的地方。[【蚂蚁】为系统 7](https://68kmla.org/forums/index.php?/topic/54476-wifi-extension-development-thread/) 写了一个 WiFi 扩展(与[相关的 GitHub](https://github.com/antscode/MacWifi/releases)

Vonets WiFi 卡的问题是必须通过浏览器进行配置。由于没有适用于传统 MAC 电脑的现代浏览器，这意味着要么拿出一台 PowerBook，要么通过你日常使用的台式电脑进行配置。WiFi 扩展解决了这个问题，它让传统的 mac 能够几乎自动地配置 Vonets 卡。这个扩展看起来也像你在现代 mac 上配置 WiFi 的方式，在工具栏上有 WiFi 图标。这是*漂亮的*，也是现代 68k mac 编程的罕见例子之一。

至于给一台 30 年前的 16MHz 处理器电脑加 WiFi 能做什么，答案是一个响亮的‘不多’。你的浏览器选择有限( [iCab](http://www.icab.de/) 好像是最好的)，但是你可以慢慢加载谷歌主页。HTTPS 是行不通的，现在互联网上充斥着数兆字节的 Javascript 代码。如果你找到一个漂亮、轻量级的网页——比如[的 Hackaday 复古版](http://retro.hackaday.com/)——你看到的是一台功能强大的网络浏览机器。当然，为 SE/30 提供 WiFi 的真正用例是在家庭网络中传输文件，但仍然是:这是苹果有史以来最好的电脑的 WiFi。