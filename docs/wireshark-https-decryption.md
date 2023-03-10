# Wireshark HTTPS 解密

> 原文：<https://hackaday.com/2022/03/22/wireshark-https-decryption/>

如果你做过网络编程或黑客，你可能用过 Wireshark。如果你没有，那么你当然应该。Wireshark 允许您捕获和分析流经网络的数据，可以将其视为网络流量的示波器。然而，从设计上来说，HTTPS 交通并没有放弃它的内容。当然，你可以看到数据包，但你不能读取它们——这就是 HTTPS 的目的之一，防止人们窥探你的流量，读取你的数据。但是如果你在调试你自己的代码呢？你知道包里应该有什么，但是由于某种原因，东西不工作了。能否[解密自己的 HTTPS 流量](https://www.trickster.dev/post/decrypting-your-own-https-traffic-with-wireshark/)？答案是肯定的，[rl1987]告诉你如何做。

不过，别担心。这不会让你窥探任何人的信息。您需要在目标浏览器或应用程序和 Wireshark 之间共享一个密钥。该方法依赖于目标应用程序，如写出其键信息的浏览器。Chrome、Firefox 和其他使用 NSS/OpenSSL 库的软件将识别 SSLKEYLOGFILE 环境变量，这将导致它们向您指定的文件生成正确的输出。

如何设置取决于你的操作系统，这篇文章的主要内容是描述如何在不同的操作系统上设置环境变量。Wireshark 理解所创建的文件，因此如果您将它指向同一个文件，您就成功了。

当然，这也让你可以窥探浏览器和插件发送的数据，如果你想知道谷歌、苹果或任何人使用加密流量发送回他们的大本营，这可能是一件好事。

Wireshark 和助手可以做很多事情，甚至蓝牙。如果你只需要回放网络数据，而不一定要分析它，[你也可以做那个](https://hackaday.com/2021/04/26/linux-fu-a-little-bit-of-network-history-repeating-itself/)。