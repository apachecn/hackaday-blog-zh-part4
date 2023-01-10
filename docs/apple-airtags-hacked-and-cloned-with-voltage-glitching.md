# 苹果 AirTags 被黑，克隆了电压故障

> 原文：<https://hackaday.com/2022/07/14/apple-airtags-hacked-and-cloned-with-voltage-glitching/>

苹果 AirTags 是很有用的小设备。他们实际上在野外使用 iPhones 作为网状网络来告诉主人 AirTag 在哪里。据 Hackster.io. 报道，现在，研究人员已经证明克隆这些设备是可能的

[研究论文](https://raw.githubusercontent.com/seemoo-lab/airtag/main/woot22-paper.pdf)解释了克隆过程，这需要物理接触硬件。为了实现黑客攻击，AirTag 内部的 Nordic nRF52832 必须有电压毛刺，以启用其调试端口。研究人员能够用相对简单的工具实现这一点，使用配有一些附加组件的 Pi Pico。

启用调试接口后，提取微控制器的固件就很简单了。然后可以将这个固件克隆到另一个标签上。该团队还尝试了其他黑客手段，比如让 AirTag 定期轮换其 ID，以避免触发内置于苹果追踪系统中的反跟踪警告。

正如研究人员解释的那样，很明显，只要航空标签基于易受此类攻击的微控制器，它们就不可能真正安全。这也不是我们看到的第一次克隆 AirTag。它们是一种有趣的设备，具有一些严重的隐私和安全问题，因此跟上这一领域的发展是值得的。

【感谢 Itay 的提示！]