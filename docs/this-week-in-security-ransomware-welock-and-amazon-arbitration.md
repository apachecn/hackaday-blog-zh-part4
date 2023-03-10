# 本周安全:勒索软件、WeLock 和亚马逊仲裁

> 原文：<https://hackaday.com/2021/06/04/this-week-in-security-ransomware-welock-and-amazon-arbitration/>

又是一周的勒索，这一次是牛肉市场被关闭，原因是俄罗斯的基础设施遭到严重攻击——但等等，事情没那么简单。让我们掩盖事实。5 月 30 日星期日的某个时候， [JBS 美国公司发现了针对他们系统的勒索软件攻击](https://www.globenewswire.com/news-release/2021/05/31/2239049/0/en/Media-Statement-JBS-USA-Cybersecurity-Attack.html)。似乎他们的响应团队做得非常好，拔掉了受影响机器的插头，并立即开始恢复。周三，[有报道称他们的大部分运营已经恢复](https://apnews.com/article/jbs-sa-lifestyle-health-coronavirus-pandemic-technology-bf82114d3f54e5be2241bd5f9a0b2639)。

联邦调查局在一份简短的声明中正式将此次袭击归咎于 REvil，又名 Sodinokibi。REvil 提供勒索软件作为服务，因此很有可能是不同的参与者实际上发起了攻击。到目前为止，最初的感染是如何发生的细节很少。虽然言下之意似乎是 JBS 没有支付赎金，但我也没有看到证实。

如果这还不足以让你了解本周的勒索病毒新闻，据报道 [Fujifilm 也受到了](https://www.bleepingcomputer.com/news/security/fujifilm-shuts-down-network-after-suspected-ransomware-attack/)的攻击，并且正在恢复他们的网络。我不能确认是否有关联，但是研究的时候发现`fujifilmusa.com`宕机了。

## WeLock 解锁

我们。锁[的锁系统有问题](https://github.com/CriticalSecurity/welock)。也就是说，一个仍然被支持的非常不安全的 API。Critical Security 的好心人发现了这个问题，并试图在今年 1 月报告这一问题，但遭到了震耳欲聋的沉默。就在一个多星期前，WeLock 移动应用程序进行了更新，引入了新的、更安全的 API，但迄今为止，遗留系统仍在运行。

那么旧的 API 到底有多糟糕呢？首先，消息数据用 3DES 加密，这种加密方式[本身被认为是不安全的](https://csrc.nist.gov/News/2017/Update-to-Current-Use-and-Deprecation-of-TDEA)。真正的问题是，3DES 是一种对称加密方案，该应用程序的每个实例都使用相同的硬编码密钥。最糟糕的是，这个密钥还用来验证 API 调用。那么蓝牙解锁请求是如何进行的呢？该应用程序进行 API 调用，指定与帐户相关联的电话号码，API 返回帐户上每个智能锁的详细信息，包括他们的每个蓝牙解锁密码！一个简单的包含这个密码的 BLE 包将打开账户上的任何锁。简而言之，我们只需要打开一个 We。亲自锁定智能锁是帐户上的电话号码。

## 亚马逊回声、录音和仲裁

围绕亚马逊回声正在酝酿一个奇怪的故事[。亚马逊 Alexa 设备总是在监听它们的“唤醒词”，实际上这意味着这些设备有时会自发记录。这些录音被使用的一个例子是在刑事案件中，](https://arstechnica.com/tech-policy/2021/06/after-75000-echo-arbitration-demands-amazon-now-lets-you-sue-it/)[这些录音被传唤](https://www.wired.com/story/star-witness-your-smart-speaker/)。亚马逊将你的私人对话存储在他们的服务器上的想法可能不会让你满意，而且在一些州这可能是非法的。显而易见的解决方案可能是集体诉讼，但亚马逊 Echo 的服务条款明确禁止集体诉讼，而是强制仲裁。

你可能没有意识到的是，当一家公司强迫客户进行仲裁时，判例法和一些州法律会将财务负担推给该公司。简而言之，亚马逊强迫我进行仲裁，所以他们要为此付出代价。这笔费用对一两个人来说不算多，但当 75，000 名用户同时请求仲裁时，这笔费用就足以让亚马逊注意到了。ToS 已经放弃了强制仲裁语言，但这一变化对已经启动的法律行动没有影响。这种方法已经成功用于对抗[门档](https://www.vox.com/2020/2/12/21133486/doordash-workers-10-million-forced-arbitration-class-action-supreme-court-backfired)、[帕特里翁](https://thelaughbutton.com/owen-benjamin-vs-patreon-lawsuit-what-are-the-possible-implications)和[优步](https://www.latimes.com/business/la-fi-uber-ipo-arbitration-miscalculation-20190508-story.html)。

## 无法撬开的锁？

构建一个无法撬开的锁的问题在于，撬锁者很聪明，并不在乎一个设计是“无法撬开”的。本周，我们在[Stuff Here]和[LockPickingLawyer]之间进行了一次合作，一对这种无法撬开的锁很快就被打败了。有趣的是，在击败每一个定制设计的锁的同时，我们的律师朋友发送了一些建议，以修复他用来进入的缺陷。我们可能会得到一个后续的尝试来修复已识别的缺陷。

几乎所有不可拆线设计的诀窍在于，它们被设计成很难同时拉紧和操纵针。在这两种锁中，当锁旋转时，这是通过将销锁定在适当位置的机构来实现的。当这些销实际上与锁定机构接合时，它们不再是可接近的。挑选它们的诀窍是什么？对于第一把锁，尽可能地向上移动锁销，并用小锤子将它们敲到位。第二把锁有点棘手，需要一个机械旁路来直接给真正的核心施加张力，这样它就很容易被撬开。

 [https://www.youtube.com/embed/2A2NY29iQdI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2A2NY29iQdI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/Ecy1FBdCRbQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Ecy1FBdCRbQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



## 一次使用

本周还带来了一系列健康的小故事，如[Kali Linux 20221.2](https://www.kali.org/blog/kali-linux-2021-2-release/)的发布。这次对侧重于渗透和取证的 Linux 发行版的更新包括了正常的包更新和错误修复，但引入了一些有趣的变化。其中包括对 Raspberry Pi 400 的全面支持，让您的网络平台；禁用特权端口，这样您就可以运行绑定到低编号端口的工具，而不会成为 root 用户；Kaboxer 的加入，这是一个基于 Docker 的容器化应用系统，可以很好地集成到`apt`包管理器中。

框架最近修复了[matroska 支持中的一对 bug](https://bugs.chromium.org/p/project-zero/issues/detail?id=2166)。其中一个错误已经被证明可以通过播放演示媒体文件来利用，所以请确保更新到 1.19.1 版本的`gst-plugins-good`包。

WordPress 插件 [Fancy Product Designer 有一个严重的漏洞](https://www.bleepingcomputer.com/news/security/critical-wordpress-plugin-zero-day-under-active-exploitation/),这个漏洞正在被大肆利用。这是一个文件上传问题，攻击者可以绕过安全措施，将可执行的 PHP 文件上传到网站。如果你管理一个运行这个插件的网站，确保它尽快更新到 4.6.9，并仔细检查可能的危害。

如果你发现自己需要检查一个混乱的二进制文件，考虑一下 Python 的`angr`。[【NapongiZero】带领我们通过](https://napongizero.github.io/blog/Defeating-Code-Obfuscation-with-Angr)建立图书馆的过程来寻找正确的信息，在这个例子中是一个密钥。这是你工具箱里的一个好工具。

最后，HaveIBeenPwned 已经[发布了他们的部分后端代码作为开源](https://www.troyhunt.com/pwned-passwords-open-source-in-the-dot-net-foundation-and-working-with-the-fbi/)。[Troy]之前曾宣布他计划将整个操作开源，但在这里评论说，这是一个比预期更大的任务，将他的单人项目打包成一个开源项目。的。NET 基金会已经介入帮助，[现在有源代码来展示他们的努力](https://github.com/HaveIBeenPwned)。作为 FLOSS 发布的第一个元素是 Pwned Passwords，这是合适的，因为我们中的许多人都过于偏执(理所当然地)而不敢在 web 表单中输入密码，并相信一切都被正确地执行了。现在您可以检查源代码，甚至离线运行整个服务。