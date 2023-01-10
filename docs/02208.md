# 超级公司:露丝·王君馨和来自消防软管的固件

> 原文：<https://hackaday.com/2019/02/22/supercon-ruth-grace-wong-and-firmware-from-the-firehose/>

固件和软件都只是代码，对吗？运行互联网规模的分布式网络内容的代码与运行个人水培设备内的微型微控制器大脑的代码会有多大不同？不分昼夜！

露丝·王君馨在前世界工作，但和一些朋友兼职做制造工程师。他们的产品有预先存在的固件，其中包含(至少)一个 bug，Ruth 的工作就是找到它。有问题的代码是由中国 PCB 工程师编写的，他非常了解电子技术，但没有软件背景，这给了 Ruth 一个直接进入最原始的嵌入式编程的机会。剧透提示:她发现了这个 bug，并且一路上学到了很多关于固件的知识。这段对话跟随她一起经历了这次冒险。

“代码有很好的文档记录，用中文写的”，但是变量名非常不具描述性。类似地，尽管 PCB 工程师完全知道什么是`24C02`,但如果你是一个软件极客，那也可能是中国人。正如你所料，网络搜索在两方面都起到了拯救作用。

这个错误最终隐藏在一个中断服务例程中的 PWM 设置代码的逻辑缺陷中，它使风扇永远无法完全打开。一旦发现，就很容易修复。但是，让你对代码库有足够深刻的理解，知道去哪里找，这是成功的五分之四。见鬼，仅设置工具链就需要一两天的时间。

如果你也是一个软件类型的人，Ruth 的演讲(嵌入在下面)将从一个熟悉的角度让你快速一瞥嵌入式固件开发这个洋葱的外层。给她快速和有价值的谈话一个手表！头发斑白的硬件老手会点头附和，甚至可能会对我们的代码在“他们”看来是什么样子有一点了解。

 [https://www.youtube.com/embed/GvD4mCa8CFM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=3&wmode=transparent](https://www.youtube.com/embed/GvD4mCa8CFM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=3&wmode=transparent)

