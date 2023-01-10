# 入侵 D-Link 固件

> 原文：<https://hackaday.com/2020/08/24/hacking-d-link-firmware/>

当[0xRickSanchez]发现一些他无法解包的 D-Link 固件时，他很想知道为什么。该固件有一个新的加密方法，这是做它的工作，防止篡改和静态分析。当然，他必须[想出如何绕过它](https://0x434b.dev/breaking-the-d-link-dir3060-firmware-encryption-recon-part-1/)，并在一系列博客文章中记录他的工作。

查看熵分析显示数据是完全随机的，这是一个很好的迹象，它要么被加密，要么被压缩。目标路由器的价格约为 200 美元，但一个类似的更便宜的路由器使用了相同的加密技术，因此这种型号成为测试的硬件选择。

一根控制台电缆提供了对路由器的访问，一个名为 imgdecrypt 的可执行文件立即引起了他的注意。将该文件转移到普通的电脑上，普通的攻击者就可以看到它是如何工作的。

你可以跟着[第二部分](https://0x434b.dev/breaking-the-d-link-dir3060-firmware-encryption-static-analysis-of-the-decryption-routine-part-2-1/)走，它在[的两个不同部分](https://0x434b.dev/breaking-the-d-link-dir3060-firmware-encryption-static-analysis-part-2/)里。最终的结果是在 [GitHub](https://github.com/0xricksanchez/dlink-decrypt) 上，但是——老实说——真正的冒险是它是如何走到一起的故事。

我们花了很多时间思考像这样的逆向工程。我们也不总是关注[路由器](https://hackaday.com/2020/07/14/high-end-ham-radio-gives-up-its-firmware-secrets/)。