# 关闭的业余无线电外围设备揭示了它的窗口秘密

> 原文：<https://hackaday.com/2020/02/16/closed-ham-radio-peripheral-reveals-its-windows-secrets/>

特隆赫姆的学生无线电协会拥有一台 Flex 6500 无线电，以及相关的 Maestro 面板外设。这是一个软件定义的无线电，Maestro 是一台包含足够运行其前端软件的嵌入式 Windows 版本的计算机。不幸的是，对于我们的挪威业余无线电爱好者朋友来说，它很少运行，甚至无法连接到需要网络登录的公共 WiFi。这尤其令人恼火，因为学生网络这样做，他们不得不创建自己的热点，所以[他们提供了一些细节](https://www.la1k.no/2020/01/08/flexradio-maestro-hacking-part-1-public-wifi-and-wallpapers/)关于他们如何能够打开它一点点来做更多的事情。

起初，他们对他们用来穿透设备防御的攻击的确切性质守口如瓶，但从那时起，他们已经发布了第二部分的全部细节。它涉及通过 Maestro 软件的 web 浏览器屏幕上的右键菜单获得对文件系统和终端的访问权限，然后使用该访问权限来更改配置，这样它就可以在网络上公开。从那里他们可以像对待一个正常的 Windows 安装一样对待它，包括把其他软件比如 SmartSDR 放到它上面。

这项工作提供了对嵌入式 Windows 设备的迷人见解，并像往常一样让我们对利用的容易程度感到惊讶。我们会说，一家公司向所有人的无线电业余爱好者提供一种功能有限的产品是一种勇敢的举动，这个社区一百多年来一直在试验和寻找任何方法来扩展他们设备的功能。或许 Flexradio 的目光投向了更大的事情。