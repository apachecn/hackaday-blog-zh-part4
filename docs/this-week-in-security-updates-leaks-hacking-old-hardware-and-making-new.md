# 本周在安全:更新，泄漏，黑客攻击旧硬件，并作出新的

> 原文：<https://hackaday.com/2021/06/18/this-week-in-security-updates-leaks-hacking-old-hardware-and-making-new/>

首先，苹果发布了一些非常老的设备的更新。好吧，2013 年的年份，但这在手机时代已经是很长的时间了。修复了三个漏洞，其中两个[据报道在野外被利用](https://thehackernews.com/2021/06/apple-issues-urgent-patches-for-2-zero.html)。CVE-2021-30761 和 CVE-2021-30762 都是 Webkit 中的缺陷，允许在访问恶意网站时执行任意代码。

第三个修复的错误非常有趣，CVE-2021-30737，ASN.1 解码器中的内存损坏。ASN.1 是一种序列化格式，用于许多不同的加密和电信协议，如 PKCS 密钥交换协议。这个 bug 是[xerub]报告的，他展示了一个针对开机后立即锁定的 iPhone 的攻击。需要闯入一部旧 iPhone？看起来现在有了一个漏洞。

> [pic.twitter.com/zf1lZMbcUU](https://t.co/zf1lZMbcUU)
> 
> —~(@ xerub)[2021 年 5 月 28 日](https://twitter.com/xerub/status/1398364882014294017?ref_src=twsrc%5Etfw)