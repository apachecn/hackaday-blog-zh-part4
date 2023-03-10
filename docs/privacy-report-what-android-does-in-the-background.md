# 隐私报告:Android 在后台做什么

> 原文：<https://hackaday.com/2021/11/18/privacy-report-what-android-does-in-the-background/>

我们已经从 90 年代和本世纪初的互联网走过了漫长的道路。不仅仅是在技术、能力和文化方面，而是在我们大多数人上网时的态度方面。在早期，大多数用户都有一种激进的冲动，除了偶尔(通常完全虚构)的 a/s/l 之外，不公开任何个人或身份信息，在易贝和亚马逊将在线购物规范化之前，甚至连输入信用卡号码都是闻所未闻的。在今天的互联网上，我们肆无忌惮地做着所有这些事情，更糟糕的是，我们大多数人都随身携带着一个设备，它不仅保存着我们所有的个人信息，还报告我们的一切，从我们的浏览习惯到我们的位置，再回到数据库中无限期存储。

众所周知，这些设备的流行移动操作系统 iOS 和 Android 都可以“呼叫总部”或者将我们的数据报告给各种服务器。但是操作系统本身到底做了多少很大程度上是一个猜测，特别是对于苹果设备来说，这些设备所做的事情只有苹果才能真正确定。虽然苹果对自己保密，因此不能完全信任，但安卓更加开放，矛盾的是，这使得公司(和恶意用户)更容易监视用户，但也使这些用户更容易自己保护自己的隐私。[多亏了最近这份关于几种不同风格的 Android 的隐私报告](https://www.scss.tcd.ie/Doug.Leith/Android_privacy_report.pdf) (PDF 警告)我们对系统应用程序在做什么，它们在收集什么信息，它们将信息发送到哪里，以及哪些版本的 Android 最适合我们这些认真对待隐私的人有了更多的了解。

## 真正的研究证实了怀疑

该报告着眼于 Android 的六种不同“风格”以及每种风格在幕后的作用。研究人员研究了三星、小米、华为和 Realme 的操作系统，这些公司也生产自己的设备，但也研究了两种替代的基于 Android 的操作系统——linea geos 和/e/OS——它们可以安装在一些设备上，如果用户选择，可以根据隐私进行定制。/e/OS 是在考虑隐私的情况下构建的，而 LineageOS 更像是一种替代产品，并不特别关注隐私。设备制造商定制的四个 Android 版本报告了大量用户数据，或者任何装有谷歌应用程序(Google Apps)包的设备都向谷歌服务器报告了似乎永无止境的用户信息流，这都不足为奇，但研究小组发现的一些具体结果绝对值得注意。

首先，这篇论文指出，所有这些公司都能轻而易举地将设备与用户联系起来。公司将设备的 IMEI 号码和其他标识符与其他用户数据相匹配，这使得将这些账户联系在一起成为一个简单的连接点游戏。这么做的主要原因是为了定向广告，但所有这些公司也会不加区别地与各种政府机构分享这些信息。它们也不是完全安全的，所以任何黑帽攻击者获得这些信息也会得到它们。这不应该太令人惊讶，但这里的新信息是，研究人员还发现这些数据在公司之间共享。例如，三星和谷歌似乎共享彼此的数据。流行的键盘应用 Swiftkey 也通过谷歌向微软发送信息。这是一个非常复杂的数据共享和服务网络，由一家公司支持另一家公司的数据收集工作。这些数据收集工作还包括一些细节，如时间戳应用程序的使用和个人联系收集。虽然操作系统实际收集的许多信息有时会令人困惑，但很明显，在这些设备上做的任何事情都可能被记录下来，就像它是一个 Twitch 流一样，因为有证据表明，几乎所有东西都可能被某人(或某个软件)监控，甚至包括用户的按键。

研究人员将这种猖獗的数据收集活动与 Android 的隐私导向版本 [/e/OS 进行了对比。/e/OS 是 LineageOS 的一个分支，专门用于隐私保护，不包含任何与 Google 相关的软件，除了关于可用更新的信息和一些其他必要信息之外，基本上不收集任何用户数据。当安装 GApps 包时，LineageOS 仅比主要制造商的 Android 产品略好，这主要是因为谷歌系统应用程序在收集用户数据方面非常普遍。不使用 GApps 包也可以使用 LineageOS，但研究人员没有采用这种方法，而是主要关注/e/OS 作为研究的去谷歌版本。](https://e.foundation/e-os/)

## 这项研究之外

虽然/e/OS 对于注重隐私的智能手机用户来说无疑是一个很好的选择，但是还有一些值得一提的地方没有包括在研究中。从这项研究得出的结论是，真正的隐私侵犯者是 GApps(只要你能避开三星等其他间谍软件。艾尔。)，可以在比/e/OS [目前支持的](https://doc.e.foundation/easy-installer#list-of-devices-supported-by-the-easy-installer)更广泛的[设备](https://wiki.lineageos.org/devices/)上安装 LineageOS。由于安装 GApps 通常是在安装 LineageOS 之后进行的，并且是一个可选步骤，因此可以简单地省略。

此外，如果你绝对离不开谷歌地图或 Gmail，有一种方法可以访问谷歌服务，而不必在你的设备上安装它们。有一个名为 MicroG 的软件包，它是 GApps 的开源替代品，允许用户访问谷歌服务，否则将可用，但限制谷歌以关键方式跟踪和收集用户数据。LineageOS 有一个名为“LineageOS for MicroG”的分支，默认情况下包括这个包而不是 GApps，尽管这个项目的维护者和 LineageOS 之间就[关注 MicroG 通过签名欺骗](https://wiki.lineageos.org/faq#will-you-enable-signature-spoofing)访问谷歌服务的方式发生了争吵。

对于那些使用谷歌 Pixel 设备的人来说，还有另外两个隐私选项。 [GrapheneOS](https://grapheneos.org/) 是以隐私为中心的 Android 版本中的佼佼者，也有许多增强安全性的改进，如应用程序沙箱，安全/验证启动的实施，通过切换禁用外设，以及其他增强功能。 [CalyxOS](https://calyxos.org/) 基于石墨烯，与石墨烯类似，但也允许使用 MicroG，并且安全性没有石墨烯高。这些版本的 Android 的唯一缺点是，它们几乎完全是为谷歌 Pixel 构建的，至少需要相信谷歌没有在他们的手机中构建某种硬件后门。

## 安卓不是唯一的选择

使用智能手机时，还有一些其他的方法可以提高在线隐私。像 [Pinephone](https://hackaday.com/2021/09/02/pining-for-a-de-googled-smartphone/) 这样的纯 Linux 手机是可以买到的，但是功能不像 Android 那么全。一些版本的 [Linux 也可用于运行安卓系统的手机](https://devices.ubuntu-touch.io/)。与任何主要服务运营商或设备制造商的工厂 Android 设备相比，iPhone 也有可能在安全性和隐私方面有所改进，尽管他们的软件是封闭源代码的，并且位于有围墙的花园后面，这使得这一点极难验证。尽管如此，如果用户不愿意跳过所有这些障碍来安装/e/OS、GrapheneOS 或 Ubuntu Touch，或者如果他们的手机有一个锁定的引导加载程序，无法刷新新的操作系统(或者如果他们的设备不支持)，那么只有在所有其他选项都用尽的情况下，才最好选择 iPhone。当然，唯一的*其他*选择是根本不拥有智能手机，这可以说是改善这些设备隐私问题的最简单方法。

该论文详细介绍了方法，还包括他们如何确定向那些对细节感兴趣的人发送哪些数据的信息。同样值得注意的是，他们指出，这些研究没有调查任何可能安装在手机上的特定应用程序，而只是查看操作系统应用程序。例如，如果你在 GrapheneOS 上安装了随机的免费游戏、银行应用或脸书，很可能会使你所有的隐私保护措施失效。这篇论文本身值得一读，即使对于那些以前没有考虑过他们的在线隐私的人来说，即使他们确实成长于 90 年代。