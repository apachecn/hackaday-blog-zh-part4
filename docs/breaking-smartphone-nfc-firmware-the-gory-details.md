# 打破智能手机 NFC 固件:血淋淋的细节

> 原文：<https://hackaday.com/2020/08/23/breaking-smartphone-nfc-firmware-the-gory-details/>

近场通信(NFC)已经存在了一段时间，例如用于访问控制、小型数据交换，当然还有移动支付系统。对于如此敏感的应用领域，安全性自然是协议的关键要素，因此任何较低级别的访问通常都受到严格的限制和保护。

这种硬件在手机中保护得特别好，支持你的 Android 设备在这里不会有太大的帮助。当然，那只是在[克里斯托弗·韦德]深入研究这个主题之前，他在今年的 DEF CON 上的 NFC 固件黑客演讲中提出了这个主题。

但在你喊出“重复！”在现在的评论中，[乔纳森·本内特]确实在最近的 [*本周在安全*](https://hackaday.com/2020/08/14/this-week-in-security-def-con-intel-leaks-snapdragon-and-a-robot-possessed/) 的文章中提到了这次谈话，但是[克里斯多夫]自从[在博客文章](https://www.pentestpartners.com/security-blog/breaking-samsung-firmware-or-turning-your-s8-s9-s10-into-a-diy-proxmark/)中写了他的谈话内容，我们认为值得一些额外的关注。

总结一下:[Christopher]拿了一个根三星 S6，在 NFC 芯片的安全固件更新过程中搜索漏洞，希望在上面运行自定义固件映像。显然，如果他没有成功，这就不值得再提两次了，他还煞费苦心地描述了他是如何做到这一点的。通过阅读他所经历的过程——从逆向工程固件到实际利用让他运行自己代码的弱点——来挑选像他这样的大脑总是令人着迷和非常有趣的。如果你是一个喜欢用代码说话的人，[漏洞就在 GitHub](https://github.com/Iskuri/Samsung-NFC-Controller-Reverse-Engineering) 上。

很自然，[克里斯托弗]向三星披露了他的发现，但被利用的漏洞——以及重现这种情况的能力——当然已经存在很长时间了。当然，你可以使用 Proxmark 设备来攻击 NFC，或者[我们在前面看到过的硬件](https://hackaday.com/2017/07/31/borrow-payment-cards-with-nfc-proxy-hardware/)，但是一部外观普通的手机肯定会减少收银台的怀疑，并可能为渗透测试人员带来全新的可能性。但话说回来，有时一个普通的应用程序就足够了，[就像我们在这个 NFC 自动售货机黑客](https://hackaday.com/2018/10/16/hacker-pops-top-on-nfc-vending-machines/)中看到的那样。

 [https://www.youtube.com/embed/aLe-xW-Ws4c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aLe-xW-Ws4c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

