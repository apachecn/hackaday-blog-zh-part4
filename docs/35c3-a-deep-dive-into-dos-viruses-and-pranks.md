# 35C3:深入了解 DOS 病毒和恶作剧

> 原文：<https://hackaday.com/2018/12/31/35c3-a-deep-dive-into-dos-viruses-and-pranks/>

哦，个人电脑革命早期允许的黑客攻击。回到 20MB 硬盘是一件大事，MS-DOS 3.1 统治着像我这样的爱好者拼凑的每一台普通米色 PC 克隆机的时代，给别人的机器“设置”做一些意想不到的事情是一件非常有趣的事情。这通常相当于找到一台无人值守的 PC——在这方面，我在大学时代居住的宿舍是一个目标丰富的环境——并将一些烦人的东西扔进 AUTOEXEC。BAT 档。当马克下一次启动机器时，迎接他的是类似反转显示或伪造硬盘格式化的东西，这让他笑逐颜开。Control-G 对我也很好。

因此，我怀着一种强烈的怀旧之情观看了[【本·卡特赖特-考克斯】最近关于 DOS 时代](https://media.ccc.de/v/35c3-9617-a_deep_dive_into_the_world_of_dos_viruses)病毒的解剖学和生理学的 35C3 演讲。给经验丰富的读者一个合理的警告，当看着一个出生在 MS-DOS 最后一次有意义的发布后近十年的人如此轻松地讨论其内部工作时，时间扭曲感是不可避免的。在对 DOS API 元素进行了很好的概述之后，他开始努力挖掘旧 DOS 病毒的档案，其中大部分都是无害的恶作剧。他构建了一些工具来查找基于系统日期触发的病毒，并使用他设计的 x86 模拟器在 1980 年至 2005 年间每天进行测试。他发现了大约 10，000 个恶意软件样本，并研究了它们的有效载荷，从新年的良好祝愿到[海豹突击队复制面食](https://knowyourmeme.com/memes/navy-seal-copypasta)迷因的怪异预示。

我们发现[Ben]的演讲是一种真正的享受，很高兴看到当代人如此深入地研究我们许多人在计算世界中崭露头角的方式。

 [https://www.youtube.com/embed/xgS1M4e_9_E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xgS1M4e_9_E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

