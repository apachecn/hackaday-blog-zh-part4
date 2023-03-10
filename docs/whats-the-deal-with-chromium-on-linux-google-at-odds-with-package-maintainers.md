# Linux 上的 Chromium 是怎么回事？谷歌与软件包维护者不和

> 原文：<https://hackaday.com/2021/01/26/whats-the-deal-with-chromium-on-linux-google-at-odds-with-package-maintainers/>

Linux 用户比大多数人更可能熟悉 Chromium，这是谷歌的免费开源网络项目，是他们广受欢迎的 Chrome 的基础。自从该项目十多年前启动以来，用户已经能够将 BSD 授权代码编译到与闭源 Chrome 几乎相同的浏览器中。因此，大多数发行版都为浏览器提供了自己的包，有些甚至包含在基本安装中。不幸的是，这种情况可能很快就会改变。

本月早些时候，Chromium 官方博客上的一篇文章解释说，一项审计发现“基于 Chromium 的第三方浏览器”使用的 API 仅供谷歌内部使用。作为回应，任何试图使用非官方 API 密钥访问 Chrome Sync 等功能的浏览器将在 3 月 15 日之后被禁止这样做。

[![](img/43db5c4158538cafcd831feb3dd8bdf2.png)](https://hackaday.com/wp-content/uploads/2021/01/linuxchromium_quote.png)

对于普通的 Chromium 用户来说，这听起来不是什么大问题。事实上，你甚至可能认为它不适合你。帖子中使用的语言听起来像是谷歌指的是从 Chromium 代码库中分离出来的浏览器，至少部分是这样的。但是这个搜索巨头也利用这个机会来编纂他们的信仰，即官方的 Chromium 版本是他们自己提供的。通过这个简单的改变，任何使用 Chromium 特定版本的人都成了不受欢迎的人。

由于对给用户一个半功能浏览器的想法不满，Chromium 的几个发行版的维护者，比如说, [Arch Linux](https://lists.archlinux.org/pipermail/arch-dev-public/2021-January/030263.html) 和 [Fedora](https://twitter.com/spotfoss/status/1351624743510827015) 已经表示，他们正在考虑将软件包从各自的库中一起取出来。随着谷歌代表[确认改变即将到来，不管社区反馈如何](https://groups.google.com/a/chromium.org/g/embedder-dev/c/NXm7GIKTNTE/m/Qxcew5lfCAAJ)，似乎更多的发行版将会跟进。

## 失信

对于大多数用户来说，这只是一个小麻烦。当然，在你的发行版的软件包库中有 Chromium 是件好事，但是去官方网站下载最新的稳定版本并不是世界末日。然而，随着谷歌不再提供 32 位版本，那些运行旧机器的人可能会猛然惊醒。在撰写本文时，他们也没有提供原生的 BSD 构建。对于那些用户来说，也许是时候给 Firefox 一个机会了。

[![](img/c6458dd2a8cec9a696f34c1b9a3f0564.png)](https://hackaday.com/wp-content/uploads/2021/01/linuxchromium_pkg.png)

Soon to be a memory of simpler times?

这个决定实际上伤害最大的人是那些花了数年时间包装谷歌开源浏览器的人。他们投入了相当多的时间和精力来编译、发布和支持定制的 Chromium，结果却让谷歌在没有征求意见的情况下把他们扫地出门。您可能认为这只是您在支持 BSD 许可的项目时所承担的风险之一，根据定义，BSD 许可的项目不提供隐含的保证，但是在这种情况下，事情就不那么简单了。

正如开发者 Eric Hameleers 在一篇冗长的博客文章中解释的那样，2013 年，谷歌 Chrome 团队为他的 Slackware Chromium 版本提供了一个专用的 API 密匙。他被授予“在您的包中包含 Google API 密钥的官方许可”，并被告知将增加该特定密钥的使用配额，“以充分支持您的用户”，因为通常分配给他的密钥将仅用于个人开发用途。Arch Linux Chromium 软件包的维护者 evangel OS fout ras[表示他在大约同一时间](https://groups.google.com/a/chromium.org/g/chromium-packagers/c/SG6jnsP4pWM/m/Kr0KlsL8CQAJ)收到了一封类似的电子邮件。

毫无疑问，谷歌知道这些人打算如何使用他们的 API 密钥。他们甚至获得了绕过 API 限制的特许，这一决定必须经过多层批准。给予特定于发行版的 Chromium 包与官方版本相同级别的功能的框架在几年前就已经达成一致并投入使用，这是肯定的。不太清楚的是，谷歌内部发生了什么，促使他们终止了这些现有的协议，只是用一篇模糊的博客帖子作为通知。

## 王国的钥匙

在这种情况下，我们可能永远不会了解全部情况，因为谷歌代表已经明确表示，这是最终的决定，所以没有必要为此担心。最终，谷歌将按照他们认为合适的方式运营他们的业务。如果他们认为允许 Chromium 的非官方版本接入他们的云服务(如 Sync)不值得，阻止他们是他们的特权。那些坚信自由和开源软件概念的人会告诉你，这是一个完美的例子，说明为什么你应该首先使用 Firefox 或其他真正自由的浏览器。

[![](img/e6367c17a0dc55140861cdda7240b8ae.png)](https://hackaday.com/wp-content/uploads/2021/01/chrome_logo.png) 另一方面，作为一个整体，黑客们并不太喜欢被告知该做什么。[寻找任意限制的非常规解决方案](https://hackaday.com/2020/10/27/community-rallies-behind-youtube-dl-after-dmca-takedown/)是游戏的名字，那么对于那些不能或不愿使用谷歌官方 Chromium 版本的人来说，还有什么选择呢？ [Foutras 提出了一个有趣的建议，即](https://groups.google.com/a/chromium.org/g/chromium-packagers/c/sPe22z7Ynrg/m/TVkLNnaeCwAJ)，至少在表面上，似乎没有与谷歌的服务条款相冲突。尽管这并不意味着他们会对此感到高兴。

简而言之，似乎没有任何技术原因导致 Chrome 的第三方版本不能简单地使用 Chrome 自带的官方 API 键。至少从 2012 年开始，这些密钥就已经为公众所知，而且在这段时间里，从未被更改过。虽然实际上*分发*一个使用这些密钥的 Chromium 版本可能是一个足以让主线分发避开的灰色区域，但一个在最终用户的机器上执行并将密钥放入相关环境变量的单独脚本可能是 Google 没有预料到的漏洞。