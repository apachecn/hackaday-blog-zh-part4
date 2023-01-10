# 家庭助手获取指纹扫描

> 原文：<https://hackaday.com/2020/05/28/home-assistant-get-fingerprint-scanning/>

生物识别技术——就像用你的指纹作为密码——当然很方便，而且如今在手机和笔记本电脑上非常普遍。虽然它们的整体安全性可能是一个问题，但它们肯定符合将偶然入侵者挡在系统之外的要求。[Lewis Barclay]有一些传感器积满灰尘，他决定使用 ESP 芯片和 MQTT 将它们与他的家庭助理连接起来。

你可以在下面的视频中看到该设备正在工作。代码在 GitHub 上，我们唯一担心的是整体安全性。当然，指纹扫描仪的安全性是有争议的，因为你听说过有人用胶带和胶水提取指纹的故事，但除此之外，如果你在网络上，似乎可以通过 MQTT 嗅探和伪造指纹信息。根据您的安全目标，这可能没什么大不了的，当然，前提是有人可能会从一开始就危害您的网络。

另一方面，这可能会让小家伙远离工作间或酒柜之类的地方。如果这孩子能黑掉 MQTT，她也许应该呆在车间里。似乎为了真正的安全，你至少需要用某种密钥方案来认证指纹读取器。

如果你想知道更多关于[指纹扫描仪如何工作](https://hackaday.com/2017/04/27/fundamentals-of-fingerprint-scanning/)的信息，有很多可以阅读。如果胶带和胶水对你来说技术含量太低，你还可以[打印一个假手指](https://hackaday.com/2019/04/08/fooling-fingerprint-scanners-with-a-resin-printer/)。这就是为什么我们[为了安全](https://hackaday.com/2015/11/10/your-unhashable-fingerprints-secure-nothing/)不建议他们。

 [https://www.youtube.com/embed/MVA19OT4Qig?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MVA19OT4Qig?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

