# 本周安全:丹卡明斯基，禁止内核开发，勒索软件，和五角大楼的 IPv4 地址

> 原文：<https://hackaday.com/2021/04/30/this-week-in-security-dan-kaminsky-banned-from-kernel-development-ransomware-and-the-pentagons-ipv4-addresses/>

本周我们从一个令人沮丧的消息开始，丹·卡明斯基因糖尿病酮症酸中毒去世，享年仅 42 岁。Dan 因注意到 DNS 响应验证中的一个弱点而出名，该弱点可能允许攻击者毒害目标 DNS 解析器的缓存。一种理论上的攻击是已知的，欺骗的 DNS 响应可能与请求冲突，但是生存时间值意味着 DNS 请求大约每八小时才发出一次。[突破是认识到](https://www.linuxjournal.com/content/understanding-kaminskys-dns-bug)TTL 限制可以通过请求虚假的子域，并针对这些请求的欺骗响应来绕过。这个简单的技术将一个需要 87 年的理论攻击转变为一个非常真实的 10 秒攻击。休息之后，看看这段视频，Dan 在视频中谈到了他为解决问题所做的努力。

 [https://www.youtube.com/embed/B0dHDD9fFM4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/B0dHDD9fFM4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



最令人印象深刻的工作可能是他说服了多少不同的供应商和维护者合作，同时保持漏洞的安静。由于问题的严重性，决定在协调补丁发布后再等 30 天发布详细信息。漏洞泄漏花了 13 天，但这仍然给了世界足够的时间来防止重大问题。

在他的一生中，丹总是有一种“走出去解决问题”的心态，这种心态激励着其他人。我们有今天的 DNSSEC，一半原因是因为丹顽强的幕后游说。他是一股正义的力量，一个黑客的黑客。

## 明尼苏达大学被禁止使用 Linux

一个故事已经流传了一段时间，最终导致明尼苏达大学全面禁止任何人发送内核补丁。这个极端的步骤是由于已知的坏补丁被发送到内核中。最初的想法是测试内核是否容易受到恶意行为者发送的伪装成补丁的攻击。[写了一篇关于考试的论文](https://github.com/QiushiWu/QiushiWu.github.io/blob/main/papers/OpenSourceInsecurity.pdf)。他们建议的修正不能激发信心，特别是因为他们一开始就建议增加一个项目的行为准则，增加一个不发布恶意代码的承诺。

这篇论文发表于 2020 年，但禁令一周前刚刚颁布。为什么？在最初的事件被处理几个月后，来自同一所大学的可疑补丁再次出现。解释是这些新的补丁是由新的代码分析工具生成的，但它们似乎引入了新的错误，而不是实际修复它们。Greg KH 认为维护人员已经浪费了足够的时间来处理补丁，并宣布了禁令。我的意见是复杂的。测试内核社区抵御这种攻击有一定的效用，但是对反复出现的不良行为进行惩罚似乎也是正确的。

## 情绪的终结

Emotet 被欧洲刑警组织描述为“世界上最危险的恶意软件”。美国 DOJ 估计[有 160 万台机器是这个僵尸网络](https://www.justice.gov/opa/pr/emotet-botnet-disrupted-international-cyber-operation)的一部分，但是由于全球执法行动，[已经没有了](https://www.techworm.net/2021/04/emotet-malware-destroy-infected-pcs.html)。为了了解摧毁 Emotet 行动的规模，请注意不得不离线的[指挥和控制(C2)服务器的数量为数以百计](https://www.zdnet.com/article/emotet-worlds-most-dangerous-malware-botnet-disrupted-by-international-police-operation/)。执法行动阉割了僵尸网络，但恶意软件仍然在世界各地的机器上安装和运行。

解决方案是托管一组 C2 服务器，向所有受感染的人推送一个新模块。4 月 25 日，这个卸载模块将移除自动运行挂钩，并关闭每台受感染机器上的任何 Emotet 进程。这一过程似乎进展顺利，但清理工作仍在进行。也就是说，从被感染的机器上收集了 430 万个电子邮件地址，并且是在被查封的服务器上发现的。执法部门已经与我们的老朋友，HIBP 的[[Troy Hunt]合作，这些电子邮件现在是该服务数据库的一部分。](https://haveibeenpwned.com/)

## 勒索软件

勒索病毒新闻这几周很忙。苹果正在处理一笔 5000 万美元的勒索需求。[宏碁也面临着来自同一集团 REvil 的类似需求](https://godecrypt.com/news/security/computer-giant-acer-hit-by-50-million-ransomware-attack/)。在苹果公司的案例中，真正的漏洞似乎出现在苹果供应商之一广达电脑的系统中。有人认为 REvil 正在利用最近的 Microsoft Exchange 漏洞进入目标网络。

QNAP 设备也受到了重创。我们已经覆盖了一些漏洞，但是[勒索病毒正在积极攻击暴露在互联网上的未打补丁的 NAS 设备](https://www.qnap.com/en/security-news/2021/response-to-qlocker-ransomware-attacks-take-actions-to-secure-qnap-nas)。 [Qlocker 是一种以简单著称的攻击](https://www.bleepingcomputer.com/news/security/a-ransomware-gang-made-260-000-in-5-days-using-the-7zip-utility/)。攻击者只需使用 7zip 运行一个远程命令来生成受密码保护的档案，看起来他们在短短一周的恶意交易中赚了近 30 万美元。故事中出现了一个英雄，当[杰克·凯布尔]试图帮助一个朋友取回数据时，[发现了犯罪支付系统的一个漏洞](https://www.cyberscoop.com/jack-cable-qlocker-ransomware-recovery/)。使用事务 ID，但是将一个字符转换为大写，就足以使系统迷惑，从而放弃解密密钥。大约 50 名受害者通过这种伎俩取回了他们的数据，然后才被发现并修复。

## 五角大楼 IPv4 地址之谜

《华盛顿邮报》开始报道一个独特的发展故事。分配给美国国防部的数百万未使用的 IPv4 地址第一次突然被路由。(当心付费墙，尽管暂时关闭 Javascript 可能有助于你阅读链接的故事。)这个故事充分利用了时间，因为路线似乎是在一位总统宣誓就职和上届政府实际结束之间的几分钟内公布的。我的第一个反应是，政治被注入到一个看似简单的安全故事中，这让我很恼火。《邮报》似乎想找一个耸人听闻的故事来刊登。但是时机真的很奇怪。这是怎么回事？

首先，让我们回顾一下背景。世界上的 IPv4 地址快用完了——已经用完了，这取决于你如何计算它们。虽然从技术上来说，它们都已经被分配了，但是在互联网的早期，一些非常大的地址块被分配了，并且从未被完全使用。一个 A 类网络包含 1600 万个地址，在早期，它们像糖果一样被分发出去，国防部有几个。接下来，值得注意的是，国会已经考虑迫使国防部出售其未使用的 IP 地址。随着供应的耗尽，未使用的 IPv4 地址可以在公开市场上卖得相当高的价格。最后一个值得注意的小趣闻是，仅仅因为没有任何东西在积极地使用一个 IP 地址，仍然有发往和来自那里的网络流量。各种网络蠕虫和扫描器不断探测整个互联网，DDoS 攻击通常使用随机源地址的 UDP 数据包。探测和响应流量可能是互联网上正在发生的实时信息的宝贵来源。

现在已经有更多有见识的声音报道了，甚至还有国防部的神秘回应。对于正在发生的事情，越来越多的共识似乎是三种解释。第一种是最简单的。众所周知，IP 域名抢注会发生，如果没有人宣布 IP 空间的边界网关协议(BGP)路由，非法使用地址就容易得多。通过声明 IP 高于 BGP，国防部正在保护这些 IP。第二，如果你能提出合理的主张，证明你在使用这些资源，就很容易抵御国会剥夺资源的企图。最后，似乎国防部的某个部门正在对互联网背景噪声和反向散射进行分析，这些噪声和反向散射是由其他未使用的网络空间接收的。

还有最后一个问题:为什么这个项目是在政府执政的最后几分钟启动的？这是某种肮脏的阴谋吗？不太可能。这种规模的项目从最初的想法到实施需要相当长的时间，并且可能需要高层管理人员的批准。虽然我不确定为什么这么晚才切换，但我发现，如果再晚一点，很多繁文缛节就必须再来一遍，新政府也需要批准。

## Drupal 核心缺陷

我们涵盖了 Drupal 扩展、WordPress 插件和 Joomla 插件中的缺陷。相当罕见的是其中一个项目的核心代码中存在严重的漏洞。这并不是说它不会发生。例如， [Drupal 在其核心代码](https://www.drupal.org/sa-core-2021-002)中有一个跨站点脚本漏洞。XSS 通常显示为一个用户在评论中注入 javascript 的方式，当其他用户访问网站时执行。这可能是良性的，就像一个用户突然成为 myspace 上最友好的帐户，也可能是恶意的，当网站所有者试图调节被困的评论时，评论者变成了管理员。目前还没有太多的细节，但是请确保您的 Drupal 安装是最新的。

## 新旧 Linux 后门

上周，[发现了一点 Linux 恶意软件](https://www.bleepingcomputer.com/news/security/new-stealthy-linux-malware-used-to-backdoor-systems-for-years/)，然后在 2018 年提交的文件中被发现。被称为 RotaJakiro，[这个后门程序使用了一些技术来避免检测](https://blog.netlab.360.com/stealth_rotajakiro_backdoor_en/)，比如在联系命令和控制服务器时通过加密方法进行轮换。知道它已经存在了这么长时间却到现在才被注意到，这有点令人不安。幸运的是，有一些简单的危害指示器(IoCs ),比如一对文件名，以及这些文件的四种可能的 md5 和。我认为记录在系统中检查这些文件的过程会很有趣。

我首先想到的是用简单的组合`find`列出系统中的所有文件，然后用`grep`查找文件名。
`sudo find / | grep systemd-daemon`

我们可以通过去掉`grep`命令来做得更好，因为`find`已经内置了名称匹配。对于奖励积分，当找到匹配文件时，我们使用`xargs`继续计算 md5sum。

`sudo find / -name "gvfsd-helper" -o -name "systemd-daemon" | xargs md5sum`

有一个潜在的问题，如果文件夹名称包含空格或其他特殊字符，`xargs`会将这些特殊字符视为输入之间的分隔符。幸运的是，`find`和`xargs`都有一个空描述模式，其中保留了特殊字符。需要转义括号来指定`-print0`标志适用于两种指定的名称模式。

`sudo find / \( -name "gvfsd-helper" -o -name "systemd-daemon" \) -print0 | xargs -0 md5sum`

我展示了这个一行程序，并立即被提醒到`find`也有一个`-exec`标志，这使得`xargs`的使用变得多余。

`sudo find / \( -name "gvfsd-helper" -o -name "systemd-daemon" \) -exec md5sum {} \;`

这给了我们一个简单的一行程序，它将计算任何具有可疑文件名的文件的`md5sum`。如果得到匹配，将输出值与已知的 IOC 进行比较。希望我们中没有人会在我们的系统中发现这个特别讨厌的东西，但是最好知道。