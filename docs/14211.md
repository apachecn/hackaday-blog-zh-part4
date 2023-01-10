# 本周安全:Retbleed，后量子，Python-atomicwrites，和神秘的 Cuteboi

> 原文：<https://hackaday.com/2022/07/15/this-week-in-security-retbleed-post-quantum-python-atomicwrites-and-the-mysterious-cuteboi/>

“为什么我们不能拥有美好的事物”类别中的另一个条目 [Retbleed 在本周](https://comsec.ethz.ch/research/microarch/retbleed/)被宣布为又一个投机执行漏洞。这一点在 AMD 的 Zen 3 和英特尔第 9 代及更高版本的硬件中有所缓解。对于早期的设备[，在缓解方面的性能打击是相当痛苦的](https://www.phoronix.com/scan.php?page=article&item=retbleed-benchmark&num=1)。这与以前的弱点有什么不同，为什么以前的缓解措施没有涵盖这个问题？

Spectre V2 滥用 CPU 的间接分支预测，触发在给定上下文中不应该执行的代码的推测性执行。即使 CPU 最终赶上并回滚了伪执行，缓存内容中仍然会留下指纹。这个想法是，读取这些指纹会泄露攻击者进程根本不应该访问的实际数据。Linux 内核中的解决方案是“ [retpoline](https://support.google.com/faqs/answer/7625886) ”，是“返回”和“蹦床”的组合。这个小工具用一些设置代替了一个`jmp`指令，最后用一个`ret`调用代替。这似乎是一个解决问题的廉价方案。

Retbleed 带来的是一种方法，这种方法还会毒害这些返回指令的推测性执行。他们的[全文(PDF)](https://comsec.ethz.ch/wp-content/files/retbleed_sec22.pdf) 描述了这项技术，它归结为操纵处理器使用易受攻击的分支目标缓冲区(BTB)而不是更安全的返回堆栈缓冲区(RSB)。在易受攻击的英特尔系统上，这意味着用足够的数据填充 RSB，以从缓冲区中弹出实际的目标回报。当一系列的跳跃和回报平仓时，最终的回报实际上使用了 BTB，因为 RSB 已经清空，或者欠载运行。易受攻击的 AMD 系统似乎总是简单地使用 BTB 来预测回报，这使得利用变得更加容易。

Windows 机器使用更积极的缓解策略，间接分支限制推测(IBRS)，这似乎完全缓解了这个特定的问题，尽管在未来几周内可能会有更多的问题。在 Linux 上，默认情况下，retpoline 缓解最终被 IBRS 所取代，这导致了上面讨论的性能下降。

如果您在一个受影响的 CPU 上，可以使用一些内核参数来控制采取什么缓解措施。`retbleed=off`如果合适，使用现有的重新极化缓解，但不会进一步降低性能，代价是易受此攻击。默认情况下，`retbleed=auto`将使用完整的缓解措施，在不禁用同步多线程(SMT)的情况下使机器尽可能安全。最后，`retbleed=auto,nosmt`将在少数技术上要求完全缓解的型号上禁用 SMT。这不是默认设置，因为它对机器的性能影响更大。

## NIST 走向后量子时代

虽然量子密码启示录尚未实现，但各种负责标准的机构正在努力通过赞助研究和选择密码方案作为下一代标准来保持领先地位。在这种情况下， [NIST 发布了他们的后量子密码标准化进程的更新。这里的大新闻是已经选择了一些算法。猎鹰，狮身人面像，水晶-凯伯，水晶-双锂。从名字来看，参赛者中肯定有一些科幻极客。](https://csrc.nist.gov/publications/detail/nistir/8413/final)

CRYSTALS-Kyber 是一种[密钥封装机制](https://blog.cloudflare.com/post-quantum-key-encapsulation/) (KEM)，一种仅使用公开发送的消息来共享私钥的方法，类似于 Diffie-Hellman。CRYSTALS-Dilithium 和其他是签名方案，用于验证数据。我们期待这些标准在我们日常使用的不同项目和应用程序中推广开来。

## PyPI，2FA，和一个坏脾气的 Dev

为了避免安全问题，PyPI 存储库[推出了一个安全策略](https://pypi.org/security-key-giveaway/)，要求关键项目的维护者对他们的账户使用双重认证，甚至发送免费的硬件密钥。入选标准是连续六个月排名前 1%的下载量。在页面上的 FAQ 中有一个相关的问题:“一个项目可以选择退出或者以任何方式变得不重要吗？”官方的回答是，“不，一旦项目被指定为关键项目，它将无限期地保留这一指定。”至少有一个开发人员发现了一个变通办法，并带来了有趣的结果。

> 很好，我刚刚删除了 atomicwrites 包，然后上传了一个新版本。现在它不再是一个关键项目
> 
> —Markus Unterwaditzer(@ untittaker)[2022 年 7 月 8 日](https://twitter.com/untitaker/status/1545476052536942592?ref_src=twsrc%5Etfw)