# 本周安全:NSO，打印假脱机系统，和一个神秘的解密器

> 原文：<https://hackaday.com/2021/07/23/this-week-in-security-nso-print-spooler-and-a-mysterious-decryptor/>

NSO 集团最近再次出现在新闻中，有多个故事报道了他们的 Pegasus 间谍软件产品。由大赦国际牵头的研究和报告被统称为“飞马项目”。这个项目在 18 日掀起了波澜，当时多家新闻媒体报道了一份 5 万个电话号码的名单，这些号码被报道为“潜在的监控目标”在这份名单中有很多有趣的人物，比如 14 位国家元首和许多记者。

也有很多问题。比如这个列表到底是什么，它是从哪里来的？大赦国际指出，这不是一份积极成为目标的人的名单。他们报告说，在他们能够检查的与名单上的条目相关的设备中，大约 50%显示出 Pegasus 间谍软件的迹象。《卫报》是最初协调发布的一部分，有一些令人印象深刻的非细节要补充:

> 数据中电话号码的存在并不能揭示一个设备是否感染了 Pegasus 或遭受了黑客攻击。然而，该财团认为，这些数据表明 NSO 政府客户在可能的监控尝试之前就确定了潜在的目标。

亚马逊的 AWS 被命名为 Pegasus C&C 架构的一部分，作为回应，[他们已经关闭了与 NSO](https://www.vice.com/en/article/xgx5bw/amazon-aws-shuts-down-nso-group-infrastructure) 相关的账户。对他们来说， [NSO 完全否认名单的有效性。](https://www.vice.com/en/article/v7exdx/nso-says-enough-is-enough-will-no-longer-talk-to-the-press-about-damning-reports)

众所周知，NSO 工具被用来监视世界各地的人。这里真正的问题是，这些工具是否被滥用来监视特别不适当的目标，NSO 是否知道这件事，如果这些说法是真的，他们现在会做什么。如果你怀疑你的设备可能被 Pegasus 入侵，看看由大赦国际开发的移动验证工具包。

## 更多打印假脱机乐趣

在这一点上，很明显，我们应该为任何不真正需要它的 Windows 机器关闭打印假脱机程序。然而，另一个缺陷已经公布， [CVE-2021-34481](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-34481) 。这个有点奇怪。根据微软的说法，这个错误与之前的打印噩梦错误完全无关，是由[Jacob Baines]在 6 月份发现的。特别奇怪的是，[它是在研究人员的截止日期](https://arstechnica.com/gadgets/2021/07/disable-the-windows-print-spooler-to-prevent-hacks-microsoft-tells-customers/)前几周公开披露的，而且还没有打补丁。他们的建议表明，它没有在野外被开发，但似乎他们的行为好像已经公开了。

如果打印后台程序 EoP 错误还不够，那么[一个全球可读的安全帐户管理器(SAM)文件](https://arstechnica.com/gadgets/2021/07/separate-eop-flaws-let-hackers-gain-full-control-of-windows-and-linux-systems/)怎么样？该缺陷与卷影复制服务有关，在 Windows 10 和 11 机器上，允许任何用户读取整个 SAM、系统和安全文件。你能用它做什么？[首先，从一个非特权用户直接跳到系统](https://video.twimg.com/tweet_video/E6vZvfOWQAkyJuS.mp4)。

## 在 KiwiSDR 中调试后门

感谢[jpa]上周在评论中指出这一点。KiwiSDR 是一个 BeagleBone 斗篷，还有一个定制的 BeagleBone 图像，可以捕捉无线电数据，并将其放到网上供任何人收听。在讨论安全问题之前，我必须说这是一个非常棒的项目。查看[全球在线节点列表](http://kiwisdr.com/public/?s=v1.461)。

问题是[这个项目包括一个内置硬编码密码](https://arstechnica.com/gadgets/2021/07/for-years-a-backdoor-in-popular-kiwisdr-product-gave-root-to-project-developer/)的根 web shell，并且它没有被很好地记录——在论坛中的几次简短提及并不算数。SHA256 编码的密码很难破解，但正如 Ars 指出的那样，任何连接都是通过 HTTP 进行的，因此数据包嗅探的一个实例就会泄露密码。值得称赞的是，开发者现在已经在[网站主页](http://kiwisdr.com/)上发布了警告，称之前的版本存在安全漏洞。Github 上最新提交的[中的一个简短讨论表明，更完整的披露即将到来](https://github.com/jks-prv/Beagle_SDR_GPS/commit/0edf5fcfb99fdffa2058c86f60c855a306a857ee#commitcomment-53548062)。(您可能需要滚动到页面底部才能找到评论。具有讽刺意味的是，我认为任何用户都不会对此有问题，只要它被很好地记录、选择加入，并且实现得更好一点。

## Linux 文件系统漏洞

这是一个奇怪的问题。就公开披露而言，它始于[一则新闻，一个登录的用户可以通过一个包含很长路径名的 SystemD 缺陷使 Linux 系统](https://www.zdnet.com/article/nasty-linux-systemd-security-bug-revealed/)崩溃。这是一个恼人的错误，但它变得更奇怪。Qualsys 的研究人员在试图实现[完全跳转到 root exploit](https://blog.qualys.com/vulnerabilities-threat-research/2021/07/20/sequoia-a-local-privilege-escalation-vulnerability-in-linuxs-filesystem-layer-cve-2021-33909) 时偶然发现了它。这种利用是一个整数可以溢出一个非常长的路径。路径字符串需要长达 1 GB。通过在这条疯狂的路径上安装然后删除某些东西，溢出允许越界写入。[PoC 可用，](https://www.qualys.com/2021/07/20/cve-2021-33909/cve-2021-33909-crasher.c)所以请确保获得您的发行版提供的最新内核。

## 今年的 0 天活动

谷歌的威胁分析小组[发布了一份报告](https://blog.google/threat-analysis-group/how-we-protect-users-0-day-attacks/),对今年活跃使用的三个使用 0 天漏洞的活动进行了深入分析。第一个是一个电子邮件活动，似乎是在亚美尼亚进行的，使用了 CVE-2021-21166 和 CVE-2021-30551，这两个都是 Chrome 中的漏洞。在可能是同一场运动的一部分中，受害者被发送了使用 ActiveX 或 VBA 宏来启动 IE 11 并触发 CVE-2021-33742 的微软 Office 文档。

讨论的最后一个活动更有趣一些，因为它使用了 Safari 0-day 来感染 iOS 上的浏览器。这一条[被认为来自俄罗斯 APT29](https://arstechnica.com/gadgets/2021/07/solarwinds-hackers-used-an-ios-0-day-to-steal-google-and-microsoft-credentials/) ，通过 LinkedIn 消息针对西欧官员。该漏洞没有与沙盒逃逸相结合，只是在浏览器的范围内运行，从访问的每个页面获取信息。

## Windows Hello 被照片骗了

Windows 你好。这并不是独一无二的，iPhone 也有通过面部识别解锁的功能，一些 Android 手机也有这个功能。Windows 系统的电脑和手机有着本质的区别。手机上的摄像头是一个已知的可信实体。任何设备都可以自称是台式机或笔记本电脑上的网络摄像头。Windows Hello 接受任何网络摄像头设备，[这导致了一些明显的安全问题](https://arstechnica.com/information-technology/2021/07/hackers-got-past-windows-hello-by-tricking-a-webcam/)。该系统使用红外成像，因此一个简单的旁路是呈现用户的红外图像。听起来，进一步的攻击应该是可能的，就像一个将自己呈现为网络摄像头的设备，但重放捕获的目标面部图像。这肯定会成为进一步研究的有趣课题。

## REvil 解密程序

在 REvil 神秘地取下他们的招牌(也就是消失和停业)后，Kaseya 勒索软件的故事有了新的发展。[已从“可信任的第三方”获得](https://arstechnica.com/gadgets/2021/07/kaseya-gets-master-decryptor-to-help-customers-still-suffering-from-revil-attack/)通用解密器，并用于恢复数据。没有关于第三方是谁的消息，相关各方也拒绝证实是否支付了赎金作为交易的一部分。希望进一步的消息会泄露出来，关于解密器是如何获得的，以及 REvil 组正在发生什么。