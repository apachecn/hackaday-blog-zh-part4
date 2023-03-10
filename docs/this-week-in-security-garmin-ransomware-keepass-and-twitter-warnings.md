# 本周安全:Garmin 勒索软件、KeePass 和 Twitter 警告

> 原文：<https://hackaday.com/2020/08/07/this-week-in-security-garmin-ransomware-keepass-and-twitter-warnings/>

7 月 23 日，[与 Garmin 相关的多项服务被下线](https://www.bleepingcomputer.com/news/security/garmin-outage-caused-by-confirmed-wastedlocker-ransomware-attack/)，包括其呼叫中心和航空相关服务。由于 Garmin 员工泄露的信息，我们知道这次多日的中断是由 Wastedlocker 勒索软件活动引起的。四天后，Garmin 能够开始恢复服务的过程。

据报道，索要的赎金是令人垂涎的 1000 万美元。有人怀疑加尔明确实支付了赎金。泄露的解密器程序确认他们收到了解密密钥。攻击显然通过 Garmin 的网络非常广泛，因为工作站和面向公众的服务器似乎都受到了影响。让我们希望 Garmin 吸取了教训，并加强了他们的安全措施。

## KeePass

KeePass [本周](https://forum.kee.pm/t/a-critical-security-update-for-keepassrpc-is-available/3040)发布了一个更新，解决了 KeePassRPC 服务中的几个缺陷。更新公告是轻的细节，但谢天谢地，我们有完整的故事直接从[菲利普丹辛格]，[的学生发现了漏洞](https://danzinger.wien/exploiting-keepassrpc/)。这两个漏洞都存在于 SRP-6(a)密钥交换协议的实现中。

易受攻击的组件是 RPC。KeyPass 本质上是一个包含密码的简单数据库。该数据库使用用户的密码进行加密，因此没有主密码就无法检索其中包含的密码。当用户启动 KeePass 时，首先会提示他或她输入主密码，然后使用该密码对数据库进行解密。KeePassRPC 服务允许其他进程(如浏览器插件)访问现已解密的数据库。新客户端第一次尝试访问 RPC 服务时，会生成一个密钥对，并提示用户是否允许新连接。公钥被存储并标记为可信，只要数据库被解锁，就允许该客户端在将来再次请求密码。

认证协议类似于 DH 密钥交换。一个共享值被提升到密钥的幂，产生一个名为 *A* 的值。这是作为密钥交换的一部分发送的，正式规范声明它永远不允许为 0。问题是 KeePassRPC 没有正确检查 *A* ！= 0.当 *A* 被设置为 0 时，整个密钥交换中断，因为所有值最终都等于 0，因为 0^x 总是 0。这意味着任何客户端都可以欺骗已经授权的客户端。

第二个漏洞是在服务器端使用的弱随机数生成器，用于生成密钥 *b* 。该密钥基于当前日期和时间，通过伪随机函数运行。因为该函数是已知的，如果攻击者能够猜出所使用的确切时间值，那么密钥就很容易被计算出来。这并不像看起来那么简单，因为时间值是以“滴答”来度量的，每个滴答是 100 纳秒。这需要一点猜测和几千次猜测才能得出正确的值，但是如果没有任何速率限制，这个过程只需要几秒钟。

这种攻击非常严重的原因是，现代 web 浏览器允许网页上运行的 Javascript 试图连接到本地主机。如果您的 KeePass 数据库未锁定，并且您加载了一个运行恶意 JS 的页面，它可能会访问 RPC 端口，欺骗授权的 KeePass 浏览器插件，并下载您的整个 KeePass 数据库。值得庆幸的是，这个错误是私下披露的，KeePassRPC 已经更新到 1.12.1，关闭了这两个漏洞。此外，1.13 已经发布，对这种攻击和类似的攻击提供了额外的保护。

## 推特

Twitter 已经开始向一些用户显示安全警告。细节极其缺乏，但让我们看看我们能梳理出什么细节。首先，警告指出问题是 Twitter Android 应用程序中的一个漏洞，但它与 Android 漏洞有关，然后链接到 2018 年 10 月 Android 安全更新[。纵观披露的漏洞，似乎没有明显的候选相关漏洞。](https://source.android.com/security/bulletin/2018-10-01)

## KDE Ark

我们已经看到一个非常简单的技术出现在无数的安全故事中:路径横切。很简单，可以包含一个“..”作为文件路径的一部分向上移动一个目录。通常情况下，这可以包含在意想不到的地方，以绕过安全限制，或做其他意想不到的事情。归档文件也不例外，没有什么可以阻止 zip 归档文件拥有这样的路径。大多数存档程序捕捉到这种行为，不允许存档文件在写入时提取。古老的 unzip 命令是这样抱怨的:

```
# unzip relative2.zip 
Archive:  relative2.zip
warning:  skipped "../" path component(s) in tmp/../../moo
 extracting: tmp/moo

```

KDE 方舟，直到最近，并没有把这些路径当作特殊的，并且[会很高兴地把文件提取到它被指示到](https://kde.org/info/security/advisory-20200730-1.txt)的任何路径。在撰写本文时，该更新似乎还没有正式发布，所以在该更新可用之前，要警惕盲目提取存档。有一个[有用的档案库](https://github.com/jwilk/traversal-archives)，可以用来测试各种横向问题，我已经确认[中有一个特别的](https://github.com/jwilk/traversal-archives/releases/download/0/relative2.zip)(包含`tmp/../../moo`的无害 zip 文件)确实演示了 Ark 中的问题。

## 最后…

还记得[靴孔](https://hackaday.com/2020/07/31/this-week-in-security-twilio-pogotv-and-boothole/)吗？多家厂商推出了针对这个 Linux 安全引导漏洞的补丁，结果导致了[一些系统无法引导。对于 RHEL 和 CentOS，已经发布了另一轮更新包，修复了问题，并再次成为可引导系统。](https://www.zdnet.com/article/the-fixes-to-the-linux-boothole-fixes-are-in/)

罪犯会对数据库泄露做什么？显然，在出售它们之后，[它们会免费发布](https://www.bleepingcomputer.com/news/security/hacker-leaks-386-million-user-records-from-18-companies-for-free/)。如果不是被盗数据，我会称之为胜利。一旦一个漏洞赚到了卖家认为可能赚到的钱，数据被免费发布的情况并不少见。这些不是很受欢迎的网站或服务，但可能值得检查一下，看看你的数据是否包括在发布中。