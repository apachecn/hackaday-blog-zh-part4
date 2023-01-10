# 本周安全:勒索软件密钥，IOS 灾难，等等

> 原文：<https://hackaday.com/2019/07/19/this-week-in-security-ransomware-keys-ios-woes-and-more/>

还记得几周前我们谈到的 GandCrab 的结尾吗？这个故事的一个新消息是，执法机构和安全研究人员的联盟[发布了该勒索软件的解密器和主解密密钥](https://www.bleepingcomputer.com/news/security/fbi-releases-master-decryption-keys-for-gandcrab-ransomware/)。从理论上讲，研究人员能够攻破储存主密钥的指挥和控制服务器。目前还不知道这一违规行为是退休的原因，还是退休的结果。

### 苹果的安全飞地被打破了？

一个 [Youtube 视频](https://www.youtube.com/watch?v=S_rlN2IIbyM)和 [Reddit 线程](https://www.reddit.com/r/iOSBeta/comments/cbfgtb/bug_very_serious_bug_that_allows_anyone_to_view)展示了一种绕过 iPhone 的 TouchID 和 FaceID 的方法，允许任何人访问保存的密码列表。侵入这些数据的技术？重复点击菜单选项，取消安全提示。如果尝试足够快，操作系统会放弃验证，只显示密码！

iPhone 有一个板载安全芯片 Secure Enclave，旨在使这种问题几乎不可能发生。设计规范规定像密码这样的数据是加密的，解密的唯一方法是使用 Enclave。目的是减轻像这样的编程错误的影响。似乎这个问题仅限于 iOS 13 测试版，你可能会在测试版中遇到错误，但这样的错误让人对苹果安全飞地的有效性产生了一些怀疑。

### URL 方案劫持

我们的下一个话题也与 iOS 相关，尽管同样的问题可能会影响 Android 手机: [URL 方案问题](https://blog.trendmicro.com/trendlabs-security-intelligence/ios-url-scheme-susceptible-to-hijacking/)。趋势科技的研究人员研究了 iOS 如何处理冲突的应用程序 URL。在正常的`http:`和`https:`URL 之外，应用程序可以注册定制的 URL 方案，以简化进程间的通信。最简单的例子是电子邮件地址和`mailto:`方案。即使在桌面上，使用这些链接之一将打开一个不同的应用程序来处理该请求。什么会出错？

像这样使用 URL 方案的一个缺点是，不是所有的应用程序都能正确验证是什么发出了请求，iOS 允许多个应用程序使用相同的 URL 方案。在给出的示例中，恶意应用程序可以注册与目标相同的 URL 处理程序，并有效地发起中间人攻击。

### Bluekeep 和修补系统

距离远程桌面协议漏洞 Bluekeep 被揭露已经过去了五个星期。大约 20%暴露于互联网的易受攻击的系统已经被修补。Bitsight 一直在运行剩余易受攻击机器的扫描，[估计大约有 800，000 个剩余易受攻击系统](https://www.bitsight.com/blog/industry-response-to-bluekeep-vulnerability)。你可能还记得这个特别的漏洞被认为是如此的有问题，甚至国家安全局也发布了一份声明鼓励修补。到目前为止，还没有针对该漏洞的蠕虫，但据推测，至少有一些参与者已经在攻击中使用了该漏洞。