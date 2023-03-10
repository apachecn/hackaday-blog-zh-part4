# 本周安全:谷歌照片、Whatsapp 和桌面手机上的厄运

> 原文：<https://hackaday.com/2020/02/07/this-week-in-security-google-photos-whatsapp-and-doom-on-deskphones/>

Google 相册很方便。你用手机拍照录像，它们自动上传到云端。然而，如果你和我一样，每张照片都会自我提醒“云”是别人服务器的一个花哨名字。会出什么问题呢？你的一些视频[随机包含在另一个用户的下载](https://arstechnica.com/gadgets/2020/02/google-photos-bug-let-strangers-download-your-private-videos/)中怎么样？

经谷歌自己证实，这一漏洞袭击了那些使用谷歌外卖的人，这种服务允许你从谷歌应用程序下载所有数据，作为一个单一的存档。根据发送给下载谷歌照片档案的用户的通知，在 11 月 21 日至 11 月 25 日之间下载的谷歌照片档案可能包含其他用户的视频。值得注意的是，这些通知并没有发送给视频被曝光的用户。

### Whatsapp

过去几天，Whatsapp 因为几个原因出现在新闻中。我让你来决定这些故事是否相关。首先，杰夫·贝索斯的一些账户或设备似乎已经被沙特特工攻破。流行的理论是，通过 Whatsapp 发送的视频包含漏洞，当下载到贝佐斯的 iPhone 上时，会导致持久的妥协。这个理论似乎得到了[FTI](https://assets.documentcloud.org/documents/6668313/FTI-Report-into-Jeff-Bezos-Phone-Hack.pdf)的一项分析的支持。

通读这份报告……令人印象深刻。他们怀疑是泄密载体的视频从未被成功解密。没有发现实际的危害迹象，也没有发现恶意更改的系统文件。报告中发现的最接近确凿证据的东西是在潜在妥协后观察到的大量传出数据。有人质疑这一指标的实用性，罗伯特·格雷厄姆很好地驳斥了这份报告。

[![](img/610174dd0edbea5d88e38891b24ac505.png)](https://hackaday.com/wp-content/uploads/2020/02/whatsapp-crash_thumbnail.png)Whatsapp *曾*有过几个[高](https://hackaday.com/2019/05/21/this-week-in-security-whats-up-with-whatsapp-windows-xp-patches-and-cisco-is-attacked-by-the-thrangrycat/) [简档](https://hackaday.com/2019/10/11/this-week-in-security-signal-whatsapp-oauth-fishing-and-more-state-sponsored-attacks/) [漏洞](https://hackaday.com/2019/11/22/this-week-in-security-more-whatsapp-nextcry-hover-to-crash-and-android-permissions-bypass/)可能被用来实施这样的攻击。这就把我们带到了 Whatsapp 的漏洞这个话题，所以这里有一个桌面应用的漏洞。

[Gal Weizman]在 2017 年发现了一个怪异的 Whatsapp 问题。当使用网络界面，发送一条引用前一条消息的消息时，有可能操纵被引用的消息，把话放进某人的嘴里。他觉得这很有趣，但最终还是回来更认真地看看他的发现。他发现他还可以劫持链接预览横幅，给他一个跨站点脚本攻击。这本身就是一个足够严重的弱点，但 XSS 并不满足于此，[Gal]更进了一步。

Whatsapp 提供了一个原生桌面应用，使用的是电子框架。电子本质上让你以原生形式打包一个 web 应用。在引擎盖下，它只是一个与基于网络的代码捆绑在一起的浏览器。电子版的一个后果是，XSS 漏洞也可能在电子版应用程序中发挥作用。这也不例外，因为 Whatsapp 的应用程序附带了一个旧版本的电子版，旧的 Chrome 漏洞仍然存在，导致一个可行的 RCE 逃脱了电子版应用程序。

Whatsapp 已经发布了解决这些问题的更新，所以如果你已经安装了桌面 Whatsapp，请确保它是最新的！

### 我被钓鱼了

你对 haveibeenpwned.com 很熟悉。你有没有想过，如果有一种服务可以在我的一个域名遭到网络钓鱼攻击时提醒我…[我被钓鱼了](https://igotphished.abuse.ch/)是为你服务的。它旨在让公司的安全团队注册公司域。当来自其中一个域的电子邮件地址出现在网络钓鱼数据库中时，该团队会收到一封电子邮件提醒他们。

注册所需要的只是你想要监控的域名的滥用@邮件地址、邮政主管@邮件地址、noc@邮件地址或安全@邮件地址。所以 gmail 用户们，你们不走运了。如果你有自己的域名，那么也许注册这项服务是值得的。

### 思科安全被 CDPwn 终结

Nortek Security & Control 制造的一系列智能锁有一个漏洞，现在正被积极利用。这些设备上的 PHP 端点无法正确清理输入，以 root 用户身份运行，[可用于运行任意命令](https://securitynews.sonicwall.com/xmlpost/linear-emerge-e3-access-controller-actively-being-exploited/)。“card_scan+decoder.php”可以通过 http 访问，“door”参数中的任何内容都作为 root 执行。主动攻击者使用 wget 从远程服务器获取文件并运行该文件。

要远程利用这一缺陷，端点必须是可访问的，这意味着迄今为止只有具有公共 IP 地址的设备易受攻击。有限的 IPv4 地址空间和 NAT 的广泛使用再次减弱了一个真正严重的漏洞的影响。随着越来越多不太安全的设备获得自己的 IP 地址，观察 IPv6 的日益普及会发生什么将是一件有趣的事情。

### 桌面电话上的厄运

受思科 CDP(思科发现协议)的启发，Armis 的研究人员以 [CDPwn](https://www.armis.com/cdpwn/) 的名称发布了他们对思科硬件的研究。有趣的细节可以在[的白皮书](https://go.armis.com/hubfs/White-papers/Armis-CDPwn-WP.pdf)中找到，但是在我们开始之前，花点时间看看下面嵌入的视频，因为它结合了我们在 Hackaday 最喜欢的一些东西:安全漏洞，以及在意想不到的硬件上运行 Doom。

 [https://www.youtube.com/embed/dJpgoLilZQY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dJpgoLilZQY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



思科制造了数百种不同的设备，他们的卖点之一是互操作性。你把一部思科电话插入思科交换机，他们会做一些自动配置魔术，设置正确的 VLANs，等等。这些特性中的许多都依赖于思科的专有协议，其中最重要的一个就是 CDP。这种第 2 层协议允许设备相互通信，而不管它们被设置为什么 VLAN。在查看了之前发现的 CDP 缺陷后，Armis 的工作人员开始工作。他们的第一个发现是拒绝服务攻击。通知相邻设备地址的数据包缺少所描述地址数量的合理上限。一个传入的数据包可能声称描述了 30 亿个地址，目标设备在试图分配足够的内存来处理该数据包时会崩溃。

一个令人惊讶的发现是，CDP 实施似乎是为不同的思科产品线从头开始构建的。虽然这意味着单个漏洞不能在所有设备上利用，但它确实表明总体上将存在更多漏洞，并且需要更长时间来修复。例如，在 VoIP 电话中，PortID TLV (Type-LengthValue)未经适当的长度检查就被复制到静态缓冲区中。这是一个微不足道的缓冲区溢出，很容易导致利用。

Cisco 为受影响的设备提供了固件更新。这些不是特别复杂的攻击。看来，再一次，一个著名的品牌名称并不能保证质量代码运行在引擎盖下。