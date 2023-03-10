# 冠状病毒测试:CRISPR 技术将简化病毒测试

> 原文：<https://hackaday.com/2020/05/27/coronavirus-testing-crispr-technology-set-to-streamline-viral-testing/>

如果我们能回到 2020 年，从头再来，很有可能我们会做很多不同的事情。人们对新冠肺炎有很多指责，但可以肯定地说，整个事件中最大的失败之一是缺乏廉价、快速、准确的新型冠状病毒病毒检测，这是当前疫情背后的病毒。这不是因为缺乏信息；毕竟，中国科学家很早就在疫情公布了病毒基因组序列，当病毒在地球上肆虐时，世界各地的研究人员也对他们从病毒中收集的所有信息做了同样的事情。

但是利用这些信息进行有用的诊断绝非易事。最初，检测病毒的唯一方法是逆转录-聚合酶链式反应(RT-PCR)测试，这是一个繁琐的过程，需要训练有素的技术人员和装备良好的实验室，需要几天到几周才能返回结果，并且只能判断患者是否有感染。抗体检测有可能成为一种快速、简便、不需要实验室的检测，但只能用于观察患者在过去的某个时间是否感染过。

随着新冠肺炎危机的持续，我们需要的是一种兼具 PCR 的特异性和敏感性以及抗体检测的快速性和简便性的检测方法。这就是一种基于最新分子生物学方法并被称为“STOPCovid”的新检测方法的出现，它可以在现在和未来的诊断中发挥重要作用。

## 细菌免疫

在某种程度上，CRISPR 已经进入了流行的词汇，它被理解为编辑生物体基因组的一种新的强大技术，有可能成为治疗遗传疾病的一种方法。这当然是故事的很大一部分，这将在未来 15 年左右为某人赢得诺贝尔奖，但这不是故事的全部。CRISPR 基因编辑方法的根源在于细菌世界，以及这些单细胞生物如何进化出与人类免疫系统非常相似的复杂免疫系统。

随着我们对避免、检测和治疗病毒感染的重视，可能会让一些人感到惊讶的是，有成千上万种病毒已经进化成攻击细菌。据估计，这些*噬菌体，简称*或噬菌体，比它们的细菌宿主多 10 倍，这意味着地球上有大约 10 ^(30) 个噬菌体颗粒，这个数字大大超过了任何生物体的数量。就像任何其他病毒一样，如流感病毒或新型冠状病毒病毒，噬菌体的任务是找到合适的宿主，注入其遗传物质，并接管细胞的机器以制造更多的自身，通常在这个过程中摧毁宿主。

因此，显而易见，细菌进化出了检测和躲避病毒感染的机制。这就是*聚集的有规则间隔的短回文重复序列*，或 CRISPR，发挥作用的地方。CRISPR 序列本质上是从入侵噬菌体的遗传物质中剪切下来的 DNA 片段的集合。这些被称为间隔区的短序列通过一组被称为 CRISPER associate (Cas)蛋白质的酶添加到细菌基因组中。

间隔区是细菌免疫的关键。随着 CRISPR 片段中一些相邻的重复序列，间隔区被转录成互补的 RNA 片段，称为 crRNA，或 CRISPR-RNA。crRNAs 与 Cas9 等蛋白质结合，cas 9 是一种与 CRISPER 相关的酶，既可以解开 DNA，也可以切割它。来自间隔区的 crRNA 部分允许它与间隔区最初来源的噬菌体 DNA 结合，这向 Cas9 发出信号以剪断入侵的噬菌体 DNA。没有噬菌体 DNA，没有感染，并且具有整合到细菌基因组中的间隔区意味着它和它的后代具有特定噬菌体的记忆。

 [https://www.youtube.com/embed/MnYppmstxIs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MnYppmstxIs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



CRISPR 在细菌免疫中的重要性的发现自然导致了基于 CRISPR-Cas 酶学的基因工程方法，这些方法远远超过了早期主要基于限制性内切核酸酶的分子生物学技术。这些酶也是细菌免疫系统的一部分，进化成在短的特定碱基对序列上切割 DNA 有数百种可供选择，但你只能在自然发生的识别序列上进行切割，或者使用其他基因工程技术将序列插入你想要的地方。CRISPR-Cas 允许您指定剪切发生的确切位置，而不考虑顺序。

## 附带损害

CRISPR 技术令人难以置信的实用性导致了更多 Cas 酶的发现，每种酶都具有不同的特性。其中一种酶，Cas13，具有非常有趣和有用的性质。像 Cas9 一样，Cas13 使用从 CRISPR 区域转录的 crRNA 作为模板来识别入侵的噬菌体。但 Cas13 不是结合并随后切割 DNA，而是靶向噬菌体 RNA，在 rRNA 间隔区指定的序列处切割它。一旦发生这种情况，Cas13 就会变得有些草率，不管序列如何，都会切割任何触手可及的 RNA 片段。这有点像从银行对账单上剪下你的账号，然后把所有这些小纸片放进碎纸机，以防万一。

正是 Cas13 对 RNA 的这种非特异性附带损害导致了一种被称为夏洛克的 CRISPR 方法的发展，用于*特异性高灵敏度酶促报告基因解锁*。夏洛克于 2017 年在麻省理工学院布罗德研究所的张峰实验室开发，使用微小的 RNA 报告片段，这些片段的两端都用不同的标记进行了标记。在最初的 RNA 扩增步骤后，Cas13 发现并切割其靶 RNA。一旦被激活，它就不断地切割它能找到的任何 RNA，包括加入到反应中的报告 RNA 片段。只有在靶序列存在的情况下，报道基因上的两个标记才通过这种侧链切割相互分离，这使得夏洛克能够以极高的特异性和灵敏度检测病毒感染；在最初的诊断测试中，寨卡病毒感染患者的病毒 DNA 可以检测到阿托摩尔范围内，即每毫升样本中约有 2000 个病毒拷贝。

 [https://www.youtube.com/embed/ZOoUIlLmxf4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZOoUIlLmxf4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



尽管如此，夏洛克程序仍然是一个繁琐的实验室过程。与目前新冠肺炎检测的黄金标准[逆转录酶-聚合酶链式反应](https://hackaday.com/2020/03/24/coronavirus-testing-just-the-facts/)过程一样，夏洛克的诊断检测需要训练有素的技术人员和装备精良的实验室来执行，由于需要使用多个反应管，因此存在交叉污染的可能性，并且仍会因运送样本和返回结果而受到延迟。

为了纠正这些问题，张的实验室提出了一种更简单的检测方法，称为 STOPCovid，用于一锅法检测病毒。他们优化了 RNA 扩增和 Cas19 识别及切割步骤，使其在单一温度下在一个缓冲液中同时运行，减少了每个测试样品所需的操作次数。这极大地降低了实验室出错的风险，并使该过程足够简单，甚至可以在设备简陋的实验室中进行。

## 棍子上的实验室

[![](img/60d9741037668baa959d66ca1b9898a7.png)](https://hackaday.com/wp-content/uploads/2020/05/sherlock-covid-19-detection-final-01.png)

Schematic of the STOPCovid process. Source: [STOPCovid](https://www.stopcovid.science/)

为了进一步简化这一过程，RNA 报告片段被重新设计以允许通过抗体进行检测。这似乎是朝着错误的方向迈出的一步，因为[正如我们之前讨论的](https://hackaday.com/2020/03/30/coronavirus-testing-follow-up-rapid-immunologic-testing/)一样，新冠肺炎感染的抗体检测只能检测患者是否产生了新型冠状病毒病毒的抗体，由于需要时间，这更像是感染的滞后指标。但在 STOPCovid 分析中，抗体不是用于检测病毒蛋白，而是作为一种分离切割的 RNA 标记的方法，这些标记用两种不同的蛋白标记。这开启了使用侧流分析的可能性，其中毛细管作用将反应溶液拉过其上施加有标签蛋白抗体的条带。这将允许卫生保健提供者使用类似于妊娠测试的测试条来读取 STOPCovid 分析的结果，将整个过程转变为护理点测试。

就像医学领域的任何事情一样，实验室和临床之间还有很长的路要走。必须进行审判，必须解决知识产权纠纷，必须让制造商排队。然而，与此同时，张博士和他的同事们没有等待。[他们已经向任何人](https://www.stopcovid.science/)提供了完整的 STOPCovid 方案，以及如何进行反应和解释结果的所有细节。他们非常明确地表示，目前这并不打算用于临床，但他们愿意将信息公布于众，并在以后担心细节，这一事实非常令人鼓舞。

STOPCovid 具有通过核酸分析检测当前感染的能力，结合侧流抗体测试的易用性，不仅对新冠肺炎病毒，而且对未来的病毒感染来说，它可能是病毒测试中的一场真正革命。