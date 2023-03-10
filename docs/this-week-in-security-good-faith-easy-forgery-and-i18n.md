# 本周安全:诚信，容易伪造，和 I18N

> 原文：<https://hackaday.com/2022/05/27/this-week-in-security-good-faith-easy-forgery-and-i18n/>

安全研究中有一个危险，我们之前已经讨论过几次了。如果你在一个生产系统上发现了一个安全漏洞，并且没有错误奖励，你可能已经违反了一些计算机法律。交出你发现的漏洞，你很可能会得到一句“谢谢”，但也有极小的可能你会因计算机犯罪而被起诉。美国的安全研究现在稍微安全了一点，因为[美国司法部发布了一项新政策](https://www.justice.gov/opa/pr/department-justice-announces-new-policy-charging-cases-under-computer-fraud-and-abuse-act)声明“善意的安全研究不应该被收费。”

虽然这是一种受欢迎的明智之举，但将这种保护写进法律会更好。另一个警告是，这项政策只适用于美国的联邦案件。其他国家，甚至个别州，可以自由地提出指控。尽管这是个好消息，但还是要小心。还有一些关于何为诚信的警告——如果一名研究人员利用缺陷发现进行勒索，那就不是诚信。

## 数字身份证

在澳大利亚新南威尔士州，[市民可以使用数字驾照](https://arstechnica.com/information-technology/2022/05/digital-drivers-license-used-by-4m-australians-is-a-snap-to-forge/)。这是通过在 Android 和 iOS 上提供的 NSW 服务应用程序来完成的。会出什么问题呢？这里有一个明显的问题，[自愿把手机交给执法人员](https://www.eff.org/issues/know-your-rights)是一个可怕的想法。除此之外，该应用程序还会根据存储在设备上的数据动态生成 ID 图像。在 jailboken 手机上，这很容易修改，但在任何其他 iPhone 上，人们可以通过备份和恢复来操作应用程序的数据。ServiceNSW 使用一个 4 位数的数字代码对这些数据进行加密。操纵手机上存储的数据很简单，因此 ID 也很简单。奇怪的是，在最初的拉取之后，应用程序从来没有对照官方数据库验证过它的数据存储。该应用程序甚至包括一个拉至刷新功能，声称可以更新 ID 数据。该函数更新日期、时间和 QR 码，但不更新潜在的欺骗数据。

 [https://www.youtube.com/embed/MIYyAlxoESk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MIYyAlxoESk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



修改 ID 以及假冒他人 ID 的能力意味着该应用程序使身份盗窃变得非常容易。二维码在扫描时确实会显示最新信息，但只有姓名和 18 岁以下状态。照片不是数据的一部分。偷个身份证，拍上你的照片，二维码就验了。新南威尔士州服务部已经做出回应，发布了一份声明，明确表示他们不了解该问题:

> 此问题是已知的，不会给客户信息带来风险。博主在他们的本地设备上操纵了他们自己的数字驾驶执照(DDL)信息。没有其他客户数据或数据源遭到破坏。它也不会对未经授权的访问或后端系统(如驱动器)的更改带来任何风险。重要的是，如果被篡改的许可证被警方扫描，新南威尔士州警方使用的实时检查(扫描 mobipol)将显示正确的个人信息，因为它调用驱动器。在扫描许可证时，执法部门可以清楚地看到它被篡改过。更改 DDL 是违法的。DDL 已经过网络专家的独立评估，比塑料卡更安全。

## 只是来翻译的

Bonita 是一个业务自动化平台，主要设计用于让企业用最少的代码整合工作流。这是一个 Java 应用程序，通常运行在 Tomcat 上，作为 docker 映像分布在其他通道中。那张下载量超过五百万的 Docker 图片[遇到了一个大问题](https://rhinosecuritylabs.com/application-security/cve-2022-25237-bonitasoft-authorization-bypass/)。`web.xml`文件包含过滤器节，用于控制如何处理请求。其中一对过滤器旨在匹配 i18n(国际化)文件，并在没有任何授权检查的情况下交付这些端点。这是有意义的，因为它允许用户在登录页面上更改界面语言。这是一个天真的过滤器，字面上匹配任何包含`i18ntranslation`的 url。因此，任何端点都可以加上`;i18ntranslation`，未经授权的用户就可以访问。哎呦！Docker 映像和其他版本已经过更新，可以解决该问题。

## 缩放修正，更新！

首先，如果你安装了 zoom，去检查一下版本。如果你的版本比 5.10.4 还老，就去触发更新吧。如果你在 Linux 上运行 Zoom，你可能不得不再次手动下载安装程序来更新，尽管在这种情况下这样做更安全一些。

抛开这些不谈，让我们来谈谈[可能允许远程代码执行的一系列问题(RCE)](https://arstechnica.com/information-technology/2022/05/critical-zoom-vulnerabilities-fixed-last-week-required-no-user-interaction) 。Zoom 执行 XMPP 消息传递，即~~通过 XML 传递~~消息。Zoom 还通过这个 XML 流发送控制消息。诀窍在于，服务器使用一个库来验证这些 XML 消息，而客户机使用另一个库，具有不同的特点。听起来熟悉吗？经典请求走私材料。其中一个有趣的技巧是发送一个`clusterswitch`消息，将一个客户端指向一个不同的服务器，该服务器可能被攻击者控制。

如果 MitM 攻击还不够糟糕，攻击者可以在 Windows 上发送一个“更新”,包括一个`.exe`安装程序和一个要安装的`.cab`文件。正在运行的 Zoom 客户端检查 exe 以确认它已签名，然后执行。一个现代的缩放安装程序也确认了`cab`文件签名，但是降级攻击是可能的。发一个比较老的版本，像 4.4，还有一个恶意的`.cab`文件。exe 是有签名的，所以 Zoom 运行它，这个不检查`.cab`，导致容易的 RCE。请求走私在二月份就在服务器端得到了修复，但是客户端的修复直到四月份才在 5.10.4 中发布。

## 快速提示

本周，我在帮助一个朋友思考如何为一些非正统的实用工具配置一个谷歌账户。他被迫开启双因素认证，但发现这相当痛苦，因为他经常为了开发和测试而重新安装 Android。我们想，要是你能在 Linux 机器上安装谷歌认证器，并自己备份密钥就好了。因此这个提示，因为你确实可以这样做。谷歌认证只是一个 TOTP，基于时间的一次性密码。它获取一个密钥和当前时间，并通过一个算法来产生一个(在这种情况下)6 位数的代码。

那么，如何从您的设备中获取密钥呢？在一个有根的手机上，从`sqlite`数据库中提取很容易。幸运的是，authenticator 应用程序可以将保存的密钥导出为 QR 码。捕捉二维码中包含的数据，然后[使用这个方便的 Python 脚本](https://github.com/scito/extract_otp_secret_keys)将其转换回原始秘密。(很多时候你甚至可以直接说二维码没用就能拿到秘钥。)从那里[这是一个简单的命令](https://wiki.archlinux.org/title/Google_Authenticator#Code_generation) : `oathtool --totp -b secret_key`

如果你想知道 TOTP 是如何在幕后工作的，[我们不久前写过这个。](https://hackaday.com/2017/10/16/inside-two-factor-authentication-apps)