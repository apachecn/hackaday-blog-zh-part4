# 本周安全:BGP Bogons，Chrome Zero Day，以及拯救游戏攻击

> 原文：<https://hackaday.com/2019/11/08/this-week-in-security-bgp-bogons-chrome-zero-day-and-save-game-attacks/>

我们自己的[Pat Whetman]写了一篇由密歇根大学发表的聪明的技术，在那里[激光可以用来触发一个家庭助理设备](https://hackaday.com/2019/11/06/laser-based-audio-injection-on-voice-controllable-systems/)。这是一个有趣的黑客，你应该去看看。

### 借用 IP 地址

我们已经经历了几个 IPv4 耗尽的里程碑，可用地址的缺乏真的开始显现出来，甚至对巨魔和骗子来说也是如此。一种新的方法利用了边界网关协议的弱安全性，并且[允许不良行为者临时接管保留的地址块](https://arstechnica.com/information-technology/2019/11/breaking-the-law-how-8chan-or-8kun-got-briefly-back-online/)。这些特定的提供商在俄罗斯经营，经营着他们标榜为“防弹”的网络服务，或者说对关闭请求免疫。有什么比一开始就使用不属于你的 IP 地址更好的方法来避开攻击呢？

BGP 欺骗一直是其他类型的攻击和事件的中心，比如在 2018 年，尼日利亚 ISP 的 BGP 表中的一个错误配置通过中国和俄罗斯的基础设施路由了去往谷歌服务器的流量。在这种情况下，这似乎是一个真正的错误，但几乎不能防止恶意的 BGP 表中毒。

### Chrome 零时差

谷歌 31 日发布了 Chrome 的更新，解决了两个 CVE，其中一个正被积极利用。该漏洞，CVE-2019-13720，是导致潜在免后使用的竞争条件。[卡巴斯基实验室发现这个](https://www.kaspersky.com/blog/google-chrome-zeroday-wizardopium/29126/)在韩国新闻网站上被频繁使用。攻击完全从 Javascript 运行，简单地访问一个恶意网站就足以妥协，所以如果安装了 Chrome，请更新它。

### 反兴奋剂

当你觉得自己受到反兴奋剂调查的不公平对待时，你会怎么做？显然[黑掉调查机构并发布窃取的信息](https://blogs.microsoft.com/on-the-issues/2019/10/28/cyberattacks-sporting-anti-doping/)是一种选择。当数据转储中暴露出骗局时，这种方法似乎更有效。在这种情况下，发布的数据似乎相当平凡。

### Firefox 阻止侧载扩展

Mozilla 在 31 日发布了一个有争议的公告。他们打算阻止“侧装”浏览器扩展。在此之前，可以通过将浏览器扩展复制到计算机上的特定文件夹来安装它们。一些合法的扩展使用这种安装方法，但是恶意软件、广告软件和其他不需要的软件也使用这种方法。虽然这一改变将阻止一些恶意加载项，但它确实给安装不在 Mozilla 官方商店上或未经 Mozilla 签名的扩展的用户带来了一点挑战。

正如你可能想象的那样，反应…不太积极。虽然让恶意软件更难安装当然是受欢迎的，但这让一些用例变得非常困难。我想到的一个例子是包含浏览器扩展的 Linux 包。这种变化将如何发生，还有待观察。

### 将游戏保存为攻击媒介

一个古怪的漏洞引起了我的注意，它是由 Pulse Security 的[Denis Andzakovic]发表的。他发现，由于加载了恶意修改的保存文件，最近的 indy 游戏，无标题的 Goose Game，[可以被操纵运行任意代码](https://pulsesecurity.co.nz/advisories/untitled-goose-game-deserialization)。该漏洞源于天真的反序列化例程。

如果你有兴趣深入了解。net 反序列化错误，一篇很棒的论文[被提交给 Blackhat 2012](https://media.blackhat.com/bh-us-12/Briefings/Forshaw/BH_US_12_Forshaw_Are_You_My_Type_WP.pdf) 讨论这个话题。简而言之，如果程序员不小心，反序列化例程可能会以意想不到的方式覆盖变量，潜在地导致代码执行。

乍一看，由恶意保存文件触发的漏洞似乎相对无害。修改硬盘上保存的文件所需的访问级别足以以多种更好的方式危害该计算机。进入云保存同步。例如，Steam 会自动同步用户安装位置上保存的游戏。对于我们这些可能在笔记本电脑和台式机上玩相同游戏的人来说，这是一个非常有用的功能。让保存游戏自动同步到你的所有设备是非常有用的，但如果攻击者侵入你的 Steam 帐户，你的保存游戏可能会被操纵。这导致了一个非常真实的可能性，即攻击者可以利用保存游戏漏洞将 Steam 帐户危害转化为对所有安装了 Steam 的机器的攻击。