# 利用 Twitter 的趋势算法来说明问题

> 原文：<https://hackaday.com/2022/02/05/gaming-twitters-trending-algorithm-to-make-a-point/>

如果你曾经上过 Twitter 来衡量时代精神，你会注意到，在与当天重大事件相关的趋势标签中，有时会有与单一问题原因相关的少数人感兴趣的离群值。在英国上议院的一场辩论中，当一个令人反感的原因被引用为广泛公众支持的证据时，有人担心排名算法中的一个缺陷可能是负责任的，这就留给了[马洛里·摩尔]通过获得#ThisIsAnExploit 标签趋势来证明假设，而没有大量的公众支持。

之前的一些调查工作已经证实，同等的排名可能不仅因为发布了一个标签，还因为转发了这个标签。该漏洞利用了这一点，方法是相对较少的一部分人在推特上多次转发该标签，然后转发所有其他实例。由此产生的排名收益是与标签互动的账户数量的平方，因此大大超过了真实参与者的数量。为了测试这一点，她创建了# ThisIsAnExploit 标签，并要求她的追随者这样做:在推特上转发它，并转发所有包含它的其他内容。在很短的时间内，利用成功了，击败了与英国首相在这个过程中的艰辛相关的非常高调的标签，并且大部分努力都是因为只有 50 个帐户。

我们的世界现在受到社交媒体的显著影响，因为对许多人来说，社交媒体似乎比传统的印刷媒体更值得信赖。像这样的工作很重要，因为迫切需要提醒人们，从报纸业主向科技巨头传递信息并不能带来可信度。与此同时，现在这一弱点已经暴露无遗，我们想知道黑客读者会如何从中得到乐趣。有人想看到# RaiseTheJollyWrencher 标签排在最前面吗？