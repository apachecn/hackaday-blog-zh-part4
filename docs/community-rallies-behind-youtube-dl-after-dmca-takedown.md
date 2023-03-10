# DMCA 下台后，社区集会支持 Youtube-dl

> 原文：<https://hackaday.com/2020/10/27/community-rallies-behind-youtube-dl-after-dmca-takedown/>

在这一点上，你可能已经听说了 youtube-dl 的 GitHub 库最近被移除了，以响应美国唱片工业协会(RIAA)提交的 [DMCA 撤销通知。顾名思义，这个流行的 Python 程序允许用户制作上传到 YouTube 和其他内容托管网站的音频和视频的本地副本。对于数字档案管理员、网速慢或不可靠的人以及许多黑客作家来说，这是一个重要的工具。](https://github.com/github/dmca/blob/master/2020/10/2020-10-23-RIAA.md)

听说 DMCA 关闭并随后移除了 YouTube-dl T2 存储库 T3 并未能完全遏制该程序的传播，这可能并不令人惊讶。事实上，你可以很容易地争辩说，它做了相反的事情。开发人员永远也不可能负担得起该项目目前所享有的宣传量，由于代码被授权为公共领域，用户可以自由地以他们认为合适的方式分享它。这是一个绝对不会回到瓶子里的精灵。

本着真正的黑客精神，我们已经开始看到一些颇具创造性的传播非法工具的方式。一位名为[galacticurball]的 Twitter 用户想出了一种方法来将程序转换成一对密集包装的彩虹图像，并可以在网上分享。下载 PNG 文件后，命令行 ImageMagick 咒语将图像转换成源代码的压缩 tarball。早在 2000 年，一个类似的诡计被用于[分发 DeCSS DVD 解密代码；尽管不幸的是，我们怀疑是否有人会把组成 *youtube-dl* 的大约 14000 行 Python 代码印在任何 t 恤上。](http://decss.zoy.org/)

![](img/d4ab0458a206edb798623fb535797669.png)

Screenshot of [the Tweet sharing YouTube-dl repository](https://twitter.com/GalacticFurball/status/1319765986791157761) as two images

值得注意的是，GitHub 已经正式与 RIAA 的立场保持距离。该公司在收到 DMCA 的撤销通知后被迫撤销了回购，但首席执行官 Nat Friedman 进入了该项目的 IRC 频道，并承诺正在努力尽快纠正这种情况。在最近与 TorrentFreak 的采访中，Friedman 说从 GitHub [移除 *youtube-dl* 与该公司自己的内部存档努力](https://torrentfreak.com/riaas-youtube-dl-takedown-ticks-of-developers-and-githubs-ceo-201027/)和对互联网存档的财政支持不一致。

但事实证明，在存储库重新上线之前，一些更改是必要的。虽然对于 RIAA 声明的整体有效性肯定会有一些争论，但它并不是完全没有价值。正如 DMCA 公告中指出的，该项目使用了几个自动测试，对泰勒·斯威夫特和贾斯汀·汀布莱克等艺术家的版权作品运行代码。虽然这些被公认为是非常糟糕的选择来作为官方测试案例，但 RIAA 断言整个项目的存在完全是为了下载有版权的音乐，这在现实中是没有依据的。

[Ed 注:这只是关于 GitHub 的。您仍然可以直接从源代码来源获取代码。]