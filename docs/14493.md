# 空气过滤器 DRM？黑客选择退出 NFC 贴纸

> 原文：<https://hackaday.com/2022/08/13/air-filter-drm-hacker-opts-out-with-nfc-sticker/>

[Flamingo-tech]的小米空气净化器有一个整洁的安全功能:如果需要更换过滤器，它将拒绝运行。当然，我们所说的“整洁”是指“烦人”。尤其是当净化器似乎早就判断出过滤器无用的时候。你的环境是不是比较干净，滤网还有腿？您是否使用二级预过滤器来延长实际过滤器的寿命？强硬！时间到了。这不仅低效，而且浪费。

每一个小米过滤器都包含一个具有唯一 ID 的 NTAG213 NFC 标签，并使用唯一的密码进行通信，但这个密码是如何生成的(因此如何生成新密码)不得而知。这意味着净化器无法识别兼容的标签。直到现在，那是。【Flamingo-tech】分享了[小米如何生成过滤器和净化器通信密码的发现](https://www.flamingo-tech.nl/2022/05/27/this-is-how-they-do-it/)。

[![](img/c52d542793583ff97ee1424d6e4bd25a.png)](https://hackaday.com/wp-content/uploads/2022/08/Air-filter-NFC-sticker.png)

A small NFC sticker is now all it takes to have the purifier recognize a filter as new.

[Flamingo-tech]长期以来一直是愚弄小米净化器以改变其行为的支持者。在过去，这意味着安装一个 modchip 来劫持 DRM 进程。这是在标签打印机和洗碗机上规避无意义 DRM 的经典方法，但是在这种情况下，逆向工程的努力得到了回报。

现在可以创建简单的 NFC 贴纸，并遵循所有正确的规则。根据 NFC 贴纸，一个过滤器的时间到了，但它显然仍然是好的？只需撕下 NFC 贴纸，贴上一个新的，就净化器而言，这是一个新的过滤器！

如果你对逆向工程之旅感兴趣，这里有一个包含所有数据的 GitHub 库。对于那些有兴趣购买兼容 NFC 贴纸的人，[Flamingo-tech]有一些[出售](https://www.tindie.com/products/theflamingo/10x-xiaomi-air-purifier-new-filter-nfc-sticker/)。