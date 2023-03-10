# ESP8266 解锁条形音箱中的隐藏功能

> 原文：<https://hackaday.com/2019/10/24/esp8266-unlocks-hidden-features-in-sound-bar/>

众所周知，我们购买的硬件设备往往比制造商宣传的更强大。固件锁背后隐藏的功能是一种常见的伎俩，因为它允许公司通过关闭某些功能来销售不同型号的相同设备。幸运的是，这些类型的任意限制通常很容易规避。

作为一个完美的例子，[Acuario]最近发现 LG SJ2 sound bar [有相当多的功能没有在盒子](https://hackaday.io/project/168058-lg-sj2-sound-bar-hack)上宣传。无论是因为贪婪还是懒惰，LG 并没有在放大器内部使用 ESMT AD83586B IC 提供的许多功能。该芯片通过 I2C 获得其配置，因此由于增加了 ESP8266，现在可以通过 web 界面轻松实现扩展的功能。

[![](img/b1ecc828b9935625041f8ce4b4de6ca2.png)](https://hackaday.com/wp-content/uploads/2019/10/lgsj2_detail.jpg)【acua Rio】已经发现如何打开类似模拟环绕声，或每通道音量控制的东西；所有的功能，甚至没有通过正常的控制酒吧暴露出来。但它比这更深入。LG SJ2 是一个 2.1 声道系统，无线扬声器提供左右声道。但超重低音扬声器内部的 AD83586B 实际上能够驱动两个本地连接的扬声器，尽管显然需要重新布线。

尽管[Acuario]目前正在努力解决一些不完整的文档，但仍有更多的功能需要解锁。数据表上说支持用户自定义均衡器设置，但没有给出如何实际做到这一点的例子。如果有人对这类放大器芯片有特殊的爱好，现在可能是你大放异彩的时候了。

对于黑客来说，也许没有比 Rigol 的示波器系列更好的功能锁定产品了。[从 2013 年的 2000 系列示波器](https://hackaday.com/2013/07/24/a-keygen-for-the-rigol-2000-series-scopes/)到去年的[更高端的 MSO 5000](https://hackaday.com/2018/12/19/rigol-mso5000-hacked-features-unlocked/)，解锁这些流行工具的隐藏功能已经有很长的历史了。