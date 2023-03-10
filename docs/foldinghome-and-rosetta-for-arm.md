# 折叠@Home 和 Rosetta，用于 ARM

> 原文：<https://hackaday.com/2020/08/02/foldinghome-and-rosetta-for-arm/>

大多数读者都知道各种分布式计算项目，这些项目通过在大量分布式 CPU 和 GPU 之间分配计算任务，为研究人员提供超级计算机级别的资源。其中最著名的可能是 Folding@Home 和 Rosetta，这两家公司今年在探索了解 SARS 新冠肺炎病毒的机制方面表现出色。到目前为止，这两个平台仍然只能用于英特尔衍生的架构，将大量基于 ARM 的设备排除在外。商业手机分布式计算公司 Neocortix 已经解决了这个问题，因为他们已经成功地为这两个平台开发了 ARM64 客户端，并将在适当的时候整合到官方客户端中。

因此，看起来像手机和更强大的 Raspberry Pi 板这样的普通设备现在将能够像老板一样折叠蛋白质，并且提供计算研究的整体努力将受到欢迎的推动。但是会有其他好处吗？公认的观点是，ARM 芯片比来自英特尔的同类芯片更节能，但这会带来更节能的分布式计算吗？答案是“很可能”，但这一点尚无定论，因为据说计算密集型任务会显著削弱优势。

今年早些时候，随着新冠肺炎志愿者的涌入，Folding@Home [一跃成为世界上最大的超级计算机](https://www.theguardian.com/technology/2020/apr/15/volunteers-create-worlds-fastest-supercomputer-to-combat-coronavirus)，而[我们很高兴地说，Hackaday 的读者在这个故事中发挥了他们的作用](https://hackaday.com/2020/03/18/join-team-hackaday-to-crunch-covid-19-through-foldinghome/)。撰写本文时，2020 年 7 月的统计数据显示，我们的团队在全球排名第 39 位，在 824，842 个工作单元中累积了 14，005，664，882 分。大家都做得很好，我们期待你们的手机和其他设备能提高这个数字。如果您还没有这样做，[下载客户端](https://foldingathome.org/)并加入我们..

通过 [HPCwire](https://www.hpcwire.com/2020/07/28/in-big-win-for-covid-19-research-neocortix-brings-arm-support-to-foldinghome-rosettahome/) 。感谢我们的同事[Sophi]提供的提示。