# 本周安全:Pwn2own，Zoom Zero Day，俱乐部会所数据，以及 FBI 黑客攻击狂潮

> 原文：<https://hackaday.com/2021/04/16/this-week-in-security-pwn2own-zoom-zero-day-clubhouse-data-and-an-fbi-hacking-spree/>

我们本周的第一个故事[来自 Pwn2own 竞赛](https://www.zerodayinitiative.com/blog/2021/4/2/pwn2own-2021-schedule-and-live-results)。对于任何不熟悉它的人来说，这个活动每年举行两次，并以针对最新软件的攻击的现场演示为特色。这种情况的一个例外是，当研究人员与供应商进行协调发布时，包含修复的更新就在事件发生前停止。这一次，活动是虚拟举行的，所有的尝试都可以在 Youtube 上看到[。有 23 次攻击尝试，只有两次彻底失败。部分成功 5 例，完全成功 16 例。](https://www.youtube.com/watch?v=dA3aIMgRFY8)

其中一个有趣的演示是零点击 RCE 对抗缩放。这是一次攻击中的三个漏洞。唯一的警告是，攻击必须来自公认的联系人。Pwn2Own 给每个利用漏洞的尝试总共 20 分钟，最多三次尝试，每次最多持续五分钟。大多数复杂的利用都有随机性，已知有效的利用有时并不每次都有效。变焦演示第一次没有成功，演示团队花了足够的时间来重置，他们只有足够的时间再试一次。

## 出血牙

我们差不多在六个月前第一次报道了《爆牙》。当时的细节很少，但是已经有足够的时间获得完整的报告。BleedingTooth 实际上是由[Andy Nguyen]发现的三个漏洞。第一个是 CVE 的 bad vibes-2020-24490。在处理传入的蓝牙广告数据包时缺少长度检查。这导致缓冲区溢出。这里的问题是，该漏洞只可能出现在蓝牙 5 上。

三个错误中的下一个是 CVE-2020-12352，又名坏选择。这似乎是一个逻辑错误，其中一个模糊的代码路径组装了一个包含未初始化内存的蓝牙错误包。这种信息泄漏对于利用其他漏洞来构建真正的漏洞非常重要。最后一个漏洞是 BadKarma，CVE-2020-12351。这是一个简单的类型混淆。

这里的问题是，在漏洞触发之前，类型混淆错误有使内核恐慌的趋势。这似乎是一个问题，但事实上，攻击者可以简单地请求改变通道模式以避免崩溃。这三个错误一起允许攻击者将有效负载写入内存，泄漏足够的信息来克服内核随机化，然后最终重用另一个函数作为跳转点来执行代码。查看令人毛骨悚然的细节链接。

## 思科硬件不支持

少数思科路由器有一个严重的问题，CVSS 得分为 9.8。CVE-2021-1459 是路由器 web 界面中的远程代码执行。漏洞在于预认证，由于路由器通常被用作 VPN 端点，因此大多数安装都可能存在漏洞。真正的踢球者？路由器已超过支持终止日期。官方说法是没有更新，也没有变通办法。所以，也许你可以去办公室的网络柜里找找 RV110W、RV130、RV130W 或 RV215W。找到一个，把思科的建议发给处理它或安全的人。如果是你，那么是时候买个新路由器了。

## 会所漏水

还记得上周公开的脸书泄密事件吗？[会所现在好像也有同样的问题](https://cybernews.com/security/clubhouse-data-leak-1-3-million-user-records-leaked-for-free-online/)。公共 API 公开了一些介于公共和私有之间的信息。与其对 API 抓取进行技术限制， [Clubhouse 只是在 TOS 中加入了一行关于数据抓取的内容](https://cybernews.com/security/not-ideal-from-a-privacy-standpoint-clubhouse-api-lets-anyone-scrape-public-user-data/)。显而易见，服务条款并没有阻止任何人获取数据，一个拥有 130 万用户的数据库现在可以在线使用。

## 源引擎漏洞

Steam 上的源码引擎游戏有问题。发送恶意邀请是可能的，一旦被接受，就会导致代码执行。

> 两年前，秘密俱乐部成员 [@floesen_](https://twitter.com/floesen_?ref_src=twsrc%5Etfw) 报告了一个影响所有源码引擎游戏的远程代码执行缺陷。它可以通过 Steam invite 来触发。这个还有待修补，Valve 也在阻止我们公开披露。pic.twitter.com/0FWRvEVuUX
> 
> —秘密俱乐部(@ the _ secret _ club)[2021 年 4 月 10 日](https://twitter.com/the_secret_club/status/1380868759129296900?ref_src=twsrc%5Etfw)