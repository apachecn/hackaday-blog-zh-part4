# 21 世纪的欺骗:计算器中的 WiFi

> 原文：<https://hackaday.com/2020/05/07/21st-century-cheating-wifi-in-a-calculator/>

显然，我们永远不会支持考试作弊，但有时一个设备太诱人了，不能不碰它。对[中微子]来说，它是一个旧的卡西欧计算器，碰巧有一个大小完美的太阳能电池板，可以安装一个 128×32 有机发光二极管作为替代品。但由于显示器本身不会做太多事情，他决定将它连接到一个 ESP8266，并将其全部安装在计算器的外壳内，[将它变成一个值得间谍活动的互联网连接的作弊设备](https://www.youtube.com/watch?v=xGjS5958g1g)，包括一个由磁铁而不是物理按钮控制的隐形用户界面。(视频，嵌在下面。)

**编辑更新:**请阅读[我们对该项目](https://hackaday.com/2020/05/24/dmca-takedown-issued-over-casio-code-that-wasnt/)版权索赔的后续报道。尽管人们普遍认为这个项目没有侵犯版权，但是由于这些声明，上面链接的视频和下面嵌入的视频是不可用的。目前，[的原始视频可以通过互联网档案馆](https://web.archive.org/web/20200508025108/https://www.youtube.com/watch?v=xGjS5958g1g)获得。

为了实现后者，[中微子]在计算器的两端添加了两个霍尔效应传感器和一个簧片开关。在簧片开关附近放置一块磁铁(可能藏在笔帽中)将打开显示器，在霍尔效应传感器附近放置另一块磁铁将通过显示器的界面导航，支持两种输入，分别具有长、短和多击手势。为了通过 WiFi 获取信息，ESP8266 连接到 Firebase 作为后端，允许设置预定义的内容来获取，以及通过简单的聊天程序与犯罪伙伴进行交流的可能性。

由于主要想法是将可见的修改保持在最低限度，一个缺点是为给整个系统供电的额外电池充电将需要额外的外部充电电路。但是[中微子]也有一个解决方案，只是在背面露出两根电线，这很容易被误认为是随机的焊料飞溅。当然，在某些情况下，要求 WiFi 可能也很棘手，所以你可能会考虑为自己升级移动网络。

 [https://www.youtube.com/embed/xGjS5958g1g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xGjS5958g1g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

