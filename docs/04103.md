# 本周在安全方面:大量的 IPhone 泄露，更多的 VPN 漏洞，电报泄露数据，以及@Jack 的黑客攻击

> 原文：<https://hackaday.com/2019/09/06/this-week-in-security-mass-iphone-compromise-more-vpn-vulns-telegram-leaking-data-and-the-hack-of-jack/>

在一个非常以移动为中心的部分中，我们从一个长期运行的 iPhone 开发活动的故事开始。据报道，这场运动是由中国政府发起的。攻击的归属决非无关紧要，所以让我们谨慎地说，这些攻击很可能是中国的行动。

无论如何，谷歌的 Project Zero 是第一个注意到并披露恶意网站和攻击的项目。有五个独立的漏洞链，针对 iOS 版本 10 到 12，至少有一个以前未知的 0 天漏洞在使用中。Project Zero 的报道特别详细，并且真实地记录了这些漏洞。

Project Zero 调查的有效载荷不会在设备上永久安装任何恶意软件，所以如果你怀疑自己已经被入侵，重启就足以清除你的设备。

这种攻击在复杂程度上是新颖的，同时几乎完全没有针对性。恶意代码将在访问托管站点的任何 iOS 用户的设备上运行。此次攻击中使用的 0 天漏洞的潜在价值超过 100 万美元，这些高价值攻击历来更多地针对类似的高价值目标。虽然攻击中使用的网站尚未披露，但这些网站本身显然是针对中国境内的某些民族和宗教团体的。

一旦设备被感染，有效载荷将上传照片、消息、联系人，甚至实时 GPS 信息到指挥和控制基础设施。似乎在同一次攻击中， [Android 和 Windows 设备同样成为了](https://www.forbes.com/sites/thomasbrewster/2019/09/01/iphone-hackers-caught-by-google-also-targeted-android-and-microsoft-windows-say-sources/#100f87944adf)的目标。

## 泄露电话号码的电报

默认情况下，只有您添加到通讯簿中的联系人才能看到您的号码以加密信息而闻名的 Telegram 也允许匿名通信。香港的抗议者正在利用这一功能，通过 Telegram 的公共群发信息匿名组织起来。然而，最近发现了一次数据泄露，[暴露了这些公共群组成员的电话号码](https://www.forbes.com/sites/zakdoffman/2019/08/25/chinese-agencies-crack-telegram-a-timely-warning-for-end-to-end-encryption/)。你可以想象，抗议者非常想避免被认出来。泄露是基于一个特征——Telegram 希望自动将你连接到你已经认识的其他 Telegram 用户。

> 默认情况下，您的号码仅对您作为联系人添加到地址簿中的人可见。

电报是基于电话号码的。当新用户创建帐户时，系统会提示他们上传联系人列表。如果上传的联系人之一在电报系统中已经有一个号码，这些帐户会自动连接，使电话号码变得相互可见。看到问题了吗？攻击者可以加载具有几千个电话号码的设备，将其连接到电报系统，并进入其中一个目标组。如果预加载的触点与群组成员之间存在冲突，则该号码将被输出。如果有足够的资源，这种攻击甚至可以自动化，允许进行非常大规模的信息收集活动。

在这种情况下，这种运动似乎是针对香港抗议者进行的。人们不禁会想起我们报道的第一个故事，并想知道来自被入侵设备的联系数据是否被用来部分播种这项工作的搜索池。

## “杰克的黑客”

你可能已经看到，Twitter 的首席执行官杰克[@杰克]多尔西的 Twitter [账户被黑客攻击](https://www.grahamcluley.com/twitter-ceo-jack-dorsey-hacked/)，一系列令人不快的推文从该账户发出。这似乎是[chucklingSquad]的一场持续战役，他们也瞄准了其他高知名度的账户。他们是如何设法绕过双因素认证和强密码的？云雀。Cloudhopper 于 2010 年被 Twitter 收购，是一种自动向 Twitter 发布用户短信的服务。

除了用户名和密码或安全令牌，用户只通过他们的手机号码来保护。进入端口输出和 SIM 卡交换骗局。这是两种类似的技术，可以用来窃取电话号码。port-out 骗局利用了移动电话号码的法律要求。在 port-out 骗局中，攻击者声称要切换到新的运营商。SIM 卡交换骗局是说服运营商更换新手机和新 SIM 卡。不清楚使用了哪种技术，但我怀疑是一个端口输出骗局，因为 Dorsey 几天后还没有拿回他的手机号码，而 SIM 卡交换骗局可以更快地解决。

## 谷歌的 Bug 赏金扩大了

更积极的消息是，谷歌宣布扩大他们的奖金计划。实际上，除了谷歌自己的代码之外，谷歌现在还为 Play store 上最受欢迎的应用程序提供 bug 奖金。对于有抱负的研究人员来说，这似乎是一个成熟的机会，所以去选择一个下载量超过 1 亿的应用程序，并投入其中。

一个奇怪的巧合是，这个 1 亿的数字大约是 CamScanner 因恶意行为被从 Play store 中删除时的下载量。这似乎是由第三方广告库引起的。

## 更新

[上周](https://hackaday.com/2019/08/30/this-week-in-security-vpn-gateways-attacks-in-the-wild-vlc-and-an-ip-address-caper/)我们谈到了 Devcore 及其 VPN 设备研究工作。从那以后，他们发布了他们报告的第三部分[。Pulse Secure 没有那么容易被利用的漏洞，但 Devcore 团队确实发现了一个预认证漏洞，该漏洞允许从设备文件系统读取仲裁数据。作为一次胜利，他们攻破了 Twitter 的一个易受攻击的设备，向 Twitter 的 bug bounty 计划报告了此事，并为他们的麻烦获得了最高级别的奖励。](https://devco.re/blog/2019/09/02/attacking-ssl-vpn-part-3-the-golden-Pulse-Secure-ssl-vpn-rce-chain-with-Twitter-as-case-study/)