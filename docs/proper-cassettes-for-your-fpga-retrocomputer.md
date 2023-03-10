# 适合您的 FPGA 逆向计算机的盒式磁带

> 原文：<https://hackaday.com/2020/11/10/proper-cassettes-for-your-fpga-retrocomputer/>

你可以通过一个简单的问题来判断我们社区中某个人的年龄:你最早使用的可移动数据存储介质是什么？老年人用穿孔卡片，中年人用盒式磁带，30 多岁的人用软盘，20 多岁的人用闪存卡，甚至可能是“什么是可移动存储介质？”对于在云服务中长大的孩子来说。即使对逆向计算有了新的兴趣，卡带也没有卷土重来，但也许这要归功于硬件。为 FPGA 创建盒式接口是一项经常被忽视的任务，而[是【zpekic】已经着手解决的项目](https://hackaday.io/project/175680-cassette-interface-for-fpgas)。

盒式磁带数据记录是频移键控的，二进制信息的 0 和 1 用不同的音调表示。检测这些问题的预期解决方案可能是使用傅立叶变换，但他选择了一种更简单的解决方案，即计算过零点并记录其间隔时间。产生的数据流被送入 UART，从中可以重建数据本身。所有这些都在包含 Xilinx Spartan 3A FPGA 的 Mercury FPGA 板上实现，但这项技术也可以用于其他设备。

因此，你的 FPGA 反转录计算机值得一个真正的盒式接口，现在它可以有一个。如果所有这些 2020 年代的魔法能够产生一个更稳定的 [chuntey 场](https://en.wiktionary.org/wiki/chuntey)，我们会印象特别深刻，但我们猜测这可能需要更多的工作。

最后，该项目是为了纪念南斯拉夫广播先驱[ [Zoran Modli](https://en.wikipedia.org/wiki/Zoran_Modli) ]，他在 20 世纪 80 年代的创新广播节目中播放了当时计算机的磁带软件，包括我们的黑客同事[Voja Antoni]的 [Galaksija](https://hackaday.com/2015/08/03/hacking-the-digital-and-social-system/) 。通过无线电广播软件？这是一个很酷的黑客。