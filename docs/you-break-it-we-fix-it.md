# 你弄坏它，我们修理它

> 原文：<https://hackaday.com/2022/02/26/you-break-it-we-fix-it/>

苹果的空中标签引起了轰动，但原因都是错误的。首先，他们在未经所有者允许的情况下，将所有 iPhones 变成蓝牙 LE beacon 中继器。手机监听空中标签，加密它们的位置，并将数据发送到 iCloud，标签的所有者可以解密位置并追踪它。坏人已经发现这让他们在不知情的情况下跟踪他们的目标，将所有 iPhone 用户变成跟踪的潜在帮凶，甚至更糟。

自然，苹果试图通过实施一些隐私保护功能来回应。但是它们不完美到几乎无用的程度。例如，一旦离开主人的手机一段时间，空中标签就会发出哔哔声，这肯定会提醒目标他们正在被跟踪，对吗？嗯，除非作恶者把扬声器拿出来，或者买了一个已经拆下来的扬声器——这在网上有一个惊人的市场。

[![](img/b4d499e6eddb0ef21f0c96372a13b75c.png)](https://hackaday.com/wp-content/uploads/2022/02/6210d526dcfe49b5b949f446_screen_scan_nothing_thumbnail-1.png) 如果你想知道自己被跟踪，苹果“创新了有史以来第一个主动系统，提醒你不必要的跟踪”，这几乎帮助修补了他们制造的问题，但它只能在苹果手机上运行。不清楚他们所说的“第一次”是什么意思，因为来自达姆施塔特技术大学 SeeMoo 小组的黑客和研究人员至少用了四个月的时间通过在其他 75%的手机上运行的[开源 AirGuard 项目](https://github.com/seemoo-lab/AirGuard)打败了他们。

在这一过程中，SeeMoo 集团还对 AirTag 系统进行了逆向工程，允许任何可以发送 BLE 信号的东西一起运行。这为[Fabian brunlein]的[ID 跳跃“找到你”攻击](https://hackaday.com/2022/02/22/no-privacy-cloning-the-airtag/)打开了大门，该攻击通过使用 ESP32 而不是 AirTag 来破坏所有的跟踪探测器。他的基本观点是，苹果试图在“查找我的”系统上做出的大多数隐私保证都依赖于犯罪分子使用未经修改的 AirTags，而这不太可能。

平心而论，苹果在这里赢不了。他们想建立一个追踪网络，只有好人才能追踪。但是这种设备不能辨别你是在找你丢失的钥匙还是在跟踪一个泳装模特。它不知道你让它静音是因为你不希望它在你工作的时候在你的狗脖子上嘟嘟响，还是因为你把它放在了一辆豪华汽车上，当它的主人不在的时候你想把它抬起来。这个基本问题没有技术解决方案。

但是黑客们正在修补他们能修补的漏洞，并使其他漏洞可见，这样我们至少可以就技术的权衡进行合理的讨论。苹果似乎满足于天真地打开了侵犯隐私的潘多拉魔盒。不知何故，我们得想办法关闭它。

This article is part of the Hackaday.com newsletter, delivered every seven days for each of the last 200+ weeks. It also includes our favorite articles from the last seven days that you can see on [the web version of the newsletter](https://mailchi.mp/hackaday.com/hackaday-newsletter-649368). Want this type of article to hit your inbox every Friday morning? [You should sign up](http://eepurl.com/gTMxQf)!