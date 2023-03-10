# 解锁任何(本田)汽车

> 原文：<https://hackaday.com/2022/07/08/turns-out-you-can-just-unlock-any-honda-car/>

本田汽车被发现非常容易受到新发布的[滚动 PWN 攻击](https://rollingpwn.github.io/rolling-pwn/)，让你远程打开车门甚至启动引擎。到目前为止，它只在本田汽车上得到证明，但[kevin2600]测试的十个模型中有十个是易受攻击的，这使他得出结论，市场上所有的本田汽车都可能以这种方式打开。我们只是还不知道它是否会影响其他供应商，但原则上它可能会。此漏洞已被分配了 [CVE-2021-46145。](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-46145)

[kevin2600]深入探讨了攻击的含义，但没有公布太多细节。[卫斯理李]，谁发现了同样的缺陷独立，[进入更多的技术细节](http://starvlab.qianxin.com/?p=409)。黑客似乎重放了一系列先前有效的代码，将内部 PRNG 计数器重置为旧状态，从而允许攻击者重新使用已知的先前密钥。因此，它需要对以前的钥匙链-汽车通信进行一些窃听，但这应该很容易通过廉价的 SDR 和您选择的 SBC 来设置。

如果你有一款车型受到影响，那就是坏消息，因为本田很可能无论如何都不会回应。这位研究人员几周前联系了本田客户支持，但尚未收到回复。为什么选择客户支持？因为本田没有一个安全部门来提交这样的问题。即使他们这样做了，就在几个月前，本田已经表示[他们不会对“汽车解锁”漏洞做任何形式的缓解](https://www.bleepingcomputer.com/news/security/honda-bug-lets-a-hacker-unlock-and-start-your-car-via-replay-attack/)。

就目前情况来看，所有这些受影响的本田汽车可能只是在那里接受。这不是[第一次](https://hackaday.com/2021/08/30/hacker-claims-honda-and-acura-vehicles-vulnerable-to-simple-replay-attack/)本田被发现搞砸滚动代码的实施——事实上，[今年已经是第二次了。](https://thehackernews.com/2022/03/hondas-keyless-access-bug-could-let.html)也许，这一系列漏洞只是[本田取消所有替换零件 3D 模型的报应，](https://hackaday.com/2022/04/21/the-honda-takedown-how-a-global-brand-failed-to-read-the-room/)但有一点是肯定的——他们最好建立一个适当的部门来处理安全问题。