# 超微怎么了？

> 原文：<https://hackaday.com/2019/05/14/what-happened-with-supermicro/>

早在 2018 年 10 月，一个重磅炸弹震撼了科技行业，当时彭博报道说，超微制造的一些主板上有恶意组件，用于窥探或干扰主板的运行，这些主板是在亚马逊和苹果使用的服务器上发现的。我们报道了这一事件，看看[如果这是真的](https://hackaday.com/2018/10/04/malicious-component-found-on-server-motherboards-supplied-to-numerous-companies/)会如何运作。现在七个月过去了，是时候看看事情是如何发生的了。

## 还没有证据，但有很多理论

在新闻报道后，每个人都试图获得被侵入的图像或物理服务器，以努力证实这些说法，但没有人成功地独立找到任何东西。此外，苹果和亚马逊提交了明确的否认声明，超微向 SEC 提交了一封信，告诉客户它确信这个故事是假的。然后他们雇佣了第三方审计员，他们没有发现任何篡改的证据。如果那里有什么东西，要么 6 个月后没人发现它(极不可能)，要么有一个大规模的阴谋(更不可能)。

[![](img/a12afe6cf273bad5ac9c64b60f948a8f.png)](https://hackaday.com/wp-content/uploads/2019/05/Trammell-Hudson-CCC-BMC-proof-of-concept-hack.jpg)

Trammell Hudson shows a proof of concept BMC attack on a single serial data line. He did this research following the Bloomberg report to test if the attack was plausible.

Trammell Hudson 在混沌通信大会上的一次演讲中对这个话题做了一个彻底的调查，他的演讲做得非常好，汇集了其他人和他自己的研究。虽然他同意超微的制造过程可能没有受到损害，但他指出，政府机构在重新密封和发送硬件之前拦截货物并仔细修改硬件是众所周知的。这种情况是发生在即将退出的中国还是即将进入的美国，我们不得而知。他还提到了供应链在制造前被破坏以及假芯片被送到制造商手中的可能性。

他成功地用一个基本上可以代替电路板上的电阻的单一组件入侵了 BMC，用他的概念证明证明了做彭博报告中声称正在做的事情是可行的。

## 爆炸的辐射尘

该制造商最初对其股票价值造成了巨大打击，但截至 4 月份，股价已恢复到新闻发布前的水平。在他们的季度财报中，2018 年最后三个月的销售额肯定有所下降(从上一季度的 9.52 亿美元降至 9.15 亿美元)，预计 2019 年前三个月也会出现类似的下降(数字尚未公布)。换句话说，这给超微带来了数千万美元的收入损失，对品牌的损害可能更大，但这不是致命的打击。

[![](img/0884641f8e92b4268a2ad4437fa7d855.png)](https://hackaday.com/wp-content/uploads/2019/05/super_micro_stock-themed.jpg)

Super Micro stock has returned to its pre-news level.

他们刚刚在台湾破土兴建了一座 80 万平方英尺、价值 6500 万美元的新工厂，并正在扩大其硅谷总部。这至少部分是因为一些客户出于安全考虑要求超微(和其他制造商)离开中国。也可能是因为关税使得中国的产品更加昂贵。离开中国的趋势在 10 月份之前就已经开始了，但之后加速了。

对彭博的影响基本不存在。也许他们已经失去了一点可信度，虽然很难说。在文章发表后不久，他们坚持自己的文章和研究。然而，他们没有公布更多的信息来支持他们的说法，也没有发表撤回声明。如果说有什么不同的话，那就是彭博已经双倍下注了。

在关于超微的报道发布几天后，他们发布了另一项独立的指控，这次声称主板上的以太网连接器内有恶意硬件。然而，在那之后不久，那篇文章中引用的人[说他被歪曲了](https://www.servethehome.com/yossi-appleboum-disagrees-bloomberg-is-positioning-his-research-against-supermicro/)，他并不是想单挑超微，而是说这个问题是全行业的。

自那以后，这两份报告的作者乔丹·罗伯逊和迈克尔·莱利没有为彭博发表过任何东西。也许他们正在创作他们的下一部作品，或者正在研究这部作品。

## 审查超越了超微

超微最近并不是唯一受到审查的。华为也因在他们的通信设备中隐藏后门而受到抨击。这篇报道也是彭博写的，与众不同，因为这次有了佐证。随之而来的是，华为在一些国家被禁，这开始对公司造成伤害。许多制造商正在离开中国，搬到其他国家，因为中国黑客的威胁，劳动力成本的增加，质量问题和关税的上升使得搬家越来越有吸引力。超微和华为只是这一趋势的例证。

另一方面，[思科刚刚发布了关于一个服务器](https://hackaday.com/2019/05/13/this-week-in-security-backdoors-in-cisco-switches-pgp-spoofing-in-emails-git-ransomware/)中隐藏后门的公告(以及修复它的补丁)，所以可能华为只是出现了固件 bug，没有处理好。

![](img/2b359ddd9a9204ab369d324cea2a3f75.png)

Good testing SHOULD find these fakes, but how much can you check every component?

自那以后，许多人都认为彭博声称的那种硬件黑客行为背后的理论是合理的，尽管实现起来极具挑战性。供应链管理、供应商管理以及管理复杂组件的国际供应商认证和完整性是一场噩梦，而且供应商混入一些来源可疑的组件也不是闻所未闻。

然而，这并不容易，因为有如此多的组织执行如此多的测试和验证步骤。添加新组件几乎是不可能的，因为它需要大量的更改(如更改 gerber 文件、拾取和放置程序、自动光学检查和在线测试)，但用类似但恶意的组件替换现有组件将更难检测。我们已经看到了许多[实例](https://hackaday.com/2017/07/15/lets-play-spot-the-fake-mosfet/)，其中[假冒组件](https://hackaday.com/2014/04/10/fake-audiophile-opamps-revealed/)在制造商或客户不知情的情况下[进入供应链](https://hackaday.com/2018/05/05/fail-of-the-week-never-assume-all-crystals-are-born-equal/) [，所以这是一个更可信的媒介。](https://hackaday.com/2017/12/27/a-guidebook-to-the-world-of-counterfeit-parts/)

然而，迁出中国并不能完全减轻风险，因为许多零部件只在中国制造。公司越来越警惕监控他们的供应链，并消除这种安全问题的可能性。

## 总之，没有结论

有事发生了，故事还没有结束。我们仍然没有看到彭博与超微声称的确凿证据，但他们也没有收回。经历了这一切之后，超微正在恢复，他们是众多逃离中国制造业安全风险的人之一。华为的故事仍在发展，很难判断他们是恶棍、受害者还是介于两者之间。与此同时，我们应该钻研我们的安全通信技能、防火墙规则，并监控我们的供应链，以防某个故事被证明是真的。