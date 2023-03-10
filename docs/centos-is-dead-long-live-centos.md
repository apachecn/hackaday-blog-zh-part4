# 森托斯死了，森托斯万岁

> 原文：<https://hackaday.com/2020/12/09/centos-is-dead-long-live-centos/>

12 月 8 日星期二，[红帽](https://www.redhat.com/en/blog/centos-stream-building-innovative-future-enterprise-linux)和 [CentOS](https://blog.centos.org/2020/12/future-is-centos-stream/) 宣布 CentOS 8 结束。具体来说，CentOS 8 将于 2021 年底达到寿命终止，比计划提前了 8 年。要真正理解这意味着什么，以及我们是如何走到这一步的，有必要沿着记忆之路走一趟，看看 Red Hat Enterprise Linux (RHEL)、CentOS 和 IBM 的历史是如何交织在一起的。

### 第一，历史

红帽公司成立于 1995 年，由鲍勃·扬和马克·尤因合伙经营。尤因带来了他新生的 Linux 发行版，命名为 Red Hat Linux，以尤因戴的红色软呢帽而闻名。Red Hat Linux 很快推出了一系列杀手级特性，例如 Red Hat Package Manager (RPM)、Anaconda 安装程序和 ELF 二进制文件等等。到 2003 年，红帽 Linux 分裂成两个独立的发行版，RHEL 和 Fedora 核心。RHEL 是只订阅的发行版，而 Fedora Core 是最先进的免费发行版。注意，我在我的机器上运行 Fedora 是在他们把“Core”这个名字去掉之前。

RHEL 的产品虽然是开源的，但只对付费用户或非生产环境中的开发人员开放。因为它是开源的，所以没有什么可以阻止第三方移除商标，并免费重新编译软件包。这正是 Gregory Kurtzer 和 CentOS 的其他创始成员在 2004 年所做的。CentOS 版本 2 是第一个这样的版本，为社区带来了一个企业 Linux。

我们要讲述的下一段历史发生在 2009 年，兰斯·戴维斯在这个项目中失踪了。这是一个问题，因为 Davis 拥有项目域名注册、捐赠基金和项目的一些其他知识产权。这有可能会扼杀该项目，但戴维斯最终回应了一封来自该项目的公开公开信，并同意移交控制权。危机解除。

### 变得受人尊敬

2014 年[宣布了一个重要的变化](https://lists.centos.org/pipermail/centos-announce/2014-January/020100.html)。[红帽将正式赞助](https://www.redhat.com/en/about/press-releases/red-hat-and-centos-join-forces) CentOS。几个核心的 CentOS 团队将会在 Red Hat 工资单上全职工作，Red Hat 在管理委员会中获得了三个席位，最重要的是，社区确信“CentOS Linux 平台不会改变。”这并不完全清楚，但交易的一部分包括将 CentOS 的商标和知识产权转让给 Red Hat 进行安全保管。

这种安排多年来一直运作良好。CentOS 8 于 2019 年 9 月发货，紧随 RHEL 8 之后，CentOS Stream 已宣布发布，作为下一次小更新中即将推出的内容的早期展望。CentOS 流可以被认为是一个抛光的测试频道。

IBM 在 2019 年收购了红帽。该声明的一部分是承诺红帽将忠于其开源根源，声称“红帽的使命和对开源的坚定承诺将保持不变。”即使有这样的保证，许多用户还是担心 IBM 的收购会从根本上改变 Red Hat 做生意的方式。

### 我们现在在哪里

在这种背景下，最近的消息令人不安。我们中的许多人已经将 CentOS 服务器部署到生产环境中，相信 Red Hat 的承诺，即 CentOS 8 将被支持到 2029 年。Red Hat 的声明意味着这些安装在不到 2 年后就将停止使用，唯一的升级途径是 Centos Stream，也就是 RHEL 的强制测试版。正如你所想象的，社区的反应并不积极。我们感到被背叛和欺骗。目前还不清楚这个决定是由 IBM 传下来的，还是红帽自己炮制出来的。无论如何，移交 CentOS 的控制权是一个可怕的错误，这一点已经变得非常明显。

对于我们这些更喜欢基于 RPM 的系统的人来说，那会给我们带来什么呢？Fedora 很棒，但是快速的开发节奏对于服务器部署来说很可怕。OpenSUSE Leap 是 SUSE Linux Enterprise Server 的重建版，与 CentOS 非常相似，是新部署的可行选择。

在 CentOS 公告的评论中，Gregory Kurtzer 要求对重启感兴趣的用户和开发者查看他的 slack 频道。在 8 个小时内，我们中的 250 多人出现了，想要更换 CentOS。我已经直接和 Gregory 谈过了，我可以确认 RHEL 的一个新的社区重建正在进行，名字是 [Rocky Linux](https://github.com/rocky-linux/) ，以纪念另一位已经去世的 CentOS 联合创始人之一。计划是支持从 CentOS 到 Rocky Linux 的直接过渡路径。

洛基 Linux 将与 RHEL 完全兼容。这将是 CentOS，因为它是在红帽收购之前，只是在一个新的名字。我很高兴看到项目的进展，并希望在接下来的几个月里看到一个初始版本。当它发生的时候，我们将肯定告诉你它。