# 折叠@Home 的幕后:如何用分布式计算对抗病毒？

> 原文：<https://hackaday.com/2020/03/31/behind-the-scenes-of-foldinghome-how-do-you-fight-a-virus-with-distributed-computing/>

非常感谢响应号召参与 Folding@Home 的每一个人，帮助了解导致新冠肺炎的新型冠状病毒病毒的蛋白质相互作用。FAH 研究团队[的一些成员在 Reddit](https://www.reddit.com/r/pcmasterrace/comments/flgm7q/ama_with_the_team_behind_foldinghome_coronavirus) 上主持了一个 AMA(问我任何问题)会议，为我们提供幕后细节。不出所料，前两个话题是“为什么我的电脑什么都不做？”以及“这实际上完成了什么？”

第一个比较好回答。由于人们的传播——比如团队黑客日的惊人增长——新参与者大量涌入。我们可以在排行榜上看到这种情况，但在 AMA，我们有直接来自源头的数字。在这个月之前，大约有三万名定期投稿人。此后，数百辆**和数千辆*开始投入战斗。这使他们的服务器基础设施不堪重负，导致了所谓的友军 DDoS 攻击。*

 *最简洁的信息是由折叠支持论坛的版主发布的。

> 以下是当前 Folding@Home 情况的总结:
> *我们知道工作单位短缺
> *这是因为需求增加了大约 20 倍
> *我们正在努力，希望很快找到解决方案。
> *保持机器运行，它们最终会自行折叠。
> *每当我们的服务器资源增加一倍，试图提供帮助的捐赠者数量就会增加 4 倍，超过我们所做的一切。

## 他们为什么不买更多的服务器呢？

答案可以在[折叠@家捐赠常见问题](https://foldingathome.org/about/donate/donor-funding-vs-federal-grant-funding/)上找到。他们的大部分研究拨款对资金的使用都有限制。这些限制通常不包括资本设备和基础设施支出，这意味着研究人员不能“只是”购买更多的服务器。幸运的是，他们很乐观，最近的名声也吸引了足够多的有合适资源帮助的捐赠者的注意。在撰写本文时，他们的后端基础设施已经增长，尽管还没有赶上洪水。他们还在努力，坚持住！

除了计算硬件之外，在这台分布式超级计算机的输入和输出端都有人类的局限性。Folding@Home 需要领域专家将工作单元组合起来发送到我们的计算机上，并且还需要这种专业知识来审查和解释我们提交的结果。好消息是我们的贡献极大地加快了他们的迭代周期。过去需要几周或几个月的结果现在几天内就能返回，通知下一组工作单位应该调查哪里。

> 正如所承诺的，这是我们第一次看到活动中的 [#COVID19](https://twitter.com/hashtag/COVID19?src=hash&ref_src=twsrc%5Etfw) 刺突蛋白(又名 demogorgon)，感谢 [@foldingathome](https://twitter.com/foldingathome?ref_src=twsrc%5Etfw) 。更多即将推出！【pic.twitter.com/iD2crCMHcX 
> 
> —格雷格·鲍曼(@ drgregbwman)[2020 年 3 月 16 日](https://twitter.com/drGregBowman/status/1239629911310192640?ref_src=twsrc%5Etfw)*