# 本周安全:Linux WiFi、Fortinet、Text4Shell 和可预测的 GUIDs

> 原文：<https://hackaday.com/2022/10/21/this-week-in-security-linux-wifi-fortinet-text4shell-and-predictable-guids/>

本周首先关注的是 Linux 内核无线代码中的五个漏洞。它始于来自 [TU Darmstadt](https://en.wikipedia.org/wiki/Technische_Universit%C3%A4t_Darmstadt) 的【Soenke Huster】，他在 mac80211 代码中发现了缓冲区覆盖。对 SUSE 内核工程师的私下披露导致了对内核中这个无线框架的安全检查，并发现了一些其他令人讨厌的错误。几个导致拒绝服务(DOS)，但 CVE-2022-41674，CVE-2022-42719 和 CVE-2022-42720 是远程代码执行漏洞。不幸的是，这些漏洞是在处理信标帧(宣布无线网络存在的无线数据包)时触发的。机器不一定要连接或试图连接到网络，但简单地扫描网络可能会导致危害。

13 号公布了漏洞，[15 号](https://www.phoronix.com/news/Linux-6.0.2-Point-Releases-WiFi)在主线内核正式修复。许多发行版[在 14 号](https://bugzilla.redhat.com/show_bug.cgi?id=2134470)发布了更新，所以这次的转变很快。这些缺陷都是内存管理问题，这促使一些人呼吁新合并的 Rust 框架尽快在现实世界中得到一些使用。

## Fortinet

Fortinet 的大部分产品，最著名的是 Fortigate 防火墙，在管理 HTTP/S 接口上有一个预授权认证旁路。或者简单地说，如果你能进入登录页面，你可以不需要密码就能进入。这很糟糕，但是在这一点上，你真的不应该在任何硬件上有任何全球通用的管理界面。更新的固件可用。

几天过去了，所以我们对[的根本问题和如何修复](https://www.horizon3.ai/fortios-fortiproxy-and-fortiswitchmanager-authentication-bypass-technical-deep-dive-cve-2022-40684/)有了一些了解。这很简单——传入请求上转发的 HTTP 头被无意地信任。因此，只需发送一个将`Forwarded:for`和`Forwarded:by`设置为 127.0.0.1 的请求，它就会落入用于内部 API 调用的代码逻辑中。添加一个可信的 SSH 密钥，然后砰的一声，你就成功了。哎呦。

## GitHub 令牌学习新技巧

GitHub 已经就 SSH 连接到他们的服务的密码使用发起了一场小小的战争。这有一些显而易见的好处，但缺点之一是令牌会永久地安装在您的开发机器上，它可以访问您的整个 GitHub 帐户。如果你在共享服务器上做任何开发工作，这是一个真正的问题。幸运的是，GitHub 的人们已经认识到了他们的错误，并为这些令牌推出了更具选择性的访问控制。可能是时候去审计你的 GitHub 令牌了，撤销“经典”令牌，重新生成严格的控制。

## Text4Shell

如果有什么比试图通过在政治丑闻的末尾加上“gate”来让政治丑闻看起来更糟糕的话，那就是给 Java 漏洞添加“4shell”的新趋势。在这种情况下，我们有 text4shell。奇怪的是，`StringSubstitutor.replace()`和`StringSubstitutor.replaceIn()`可以对包含的字符串进行字符串查找——并且这种查找可以运行任意的 Java 代码:

`final StringSubstitutor interpolator = StringSubstitutor.createInterpolator();
String out = interpolator.replace("${script:javascript:java.lang.Runtime.getRuntime().exec('touch /tmp/foo')}");
System.out.println(out);`

有一段时间看起来现代 JDK 版本没有受到影响，但结果是一种稍微不同的方法给我们带来了完全相同的代码执行问题。

> 你好，Erik，我收到了一些关于受此漏洞影响的 JDK 版本的问题。能否请你更新你的博客帖子，以表明所有 JDK 版本都容易受到攻击？纳斯霍恩在现代 JDK 中实际上是不可用的，但杰克斯是 pic.twitter.com/rY2J9VEZrX
> 
> —阿尔瓦罗·穆尼奥斯·🇺🇦(@ pwntester)[2022 年 10 月 18 日](https://twitter.com/pwntester/status/1582321752566161409?ref_src=twsrc%5Etfw)