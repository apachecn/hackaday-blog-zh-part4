# 知道风往哪个方向吹，天气是否会提升你的心情

> 原文：<https://hackaday.com/2022/03/31/know-which-way-the-wind-blows-whether-weather-boosts-your-mood/>

作为一项自我量化的实验，[Ayan]已经跟踪了几年的日常习惯和情绪，并发现了一些见解。喝太多咖啡会带来焦虑，而听音乐会带来动力和快乐。数据中有很强的相关性，但[Ayan]怀疑天气和空气质量等外部因素是否也起了作用。

为了找到答案，[Ayan]扩展了内置于[idea . so](https://www.notion.so/)中的定制仪表盘，增加了天气数据和一些本地传感器。在 [Balena.io](https://www.balena.io/blog/authors/ayan-pahwa/) (是的，无处不在的 Raspberry Pi SD 卡闪存工具 Etcher 的制造商)工作时，[Ayan]转向 balenaCloud，通过 organization 的 API beta 将来自(你猜对了)Raspberry Pi 的数据翻译到仪表板中。我们认为，作为一个研究笔记本和组织工具，concept 为各种基于网络的仪表板提供了很大的希望。谁知道 API 会把感兴趣的读者引向何方？

查看[完整教程](https://www.balena.io/blog/log-sensor-values-to-notion-using-balena/)，其中[Ayan]将带您了解所使用的硬件，以及将所有这些硬件连接在一起的每个步骤。[Ayan]计划添加一个咖啡机集成来自动化数据输入，并欢迎帮助为数据集成设置手动触发器。