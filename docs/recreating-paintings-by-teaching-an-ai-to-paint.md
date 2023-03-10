# 通过教人工智能绘画来重建绘画

> 原文：<https://hackaday.com/2020/06/27/recreating-paintings-by-teaching-an-ai-to-paint/>

由[Amy Zhao]和团队成员进行的[time craft](https://www.csail.mit.edu/news/using-ai-recreate-how-artists-painted-their-masterpieces)项目使用机器学习来找出一种方法，即一幅现有的画[可能最初是如何被一笔一笔地绘制成](https://xamyzhao.github.io/timecraft/)的。在[他们的论文](https://arxiv.org/pdf/2001.01026.pdf)题为“画出许多过去:合成绘画的延时视频”，他们描述了他们如何使用新绘画的现有延时视频训练一个 ML 算法，允许它以概率方式生成重建一幅已经完成的绘画所需的步骤。

[![](img/32381c7e433bbeaf97accab6576b15a2.png)](https://hackaday.com/wp-content/uploads/2020/06/timecraft_architecture.png) 概率模型是用卷积神经网络(CNN)实现的，输出时延视频，跨越数分钟。在论文中，他们提到了他们是如何受到艺术风格转移的启发，在艺术风格转移中，神经网络被用来生成特定艺术家风格的艺术作品，或者创建不同艺术家的混合作品。

大量的复杂性来自于绘画创作中使用的各种各样的技术和材料，例如使用的画笔和颜料的类型。一些现有的方法专注于这里的细节，包括基于物理的油漆和笔触模拟。这些都伴随着重要的警告，Timecraft 试图通过更高层次的方法来避免这些警告。

[![](img/5c7020ce0b4c3db07811264ca5fb76ee.png)](https://hackaday.com/wp-content/uploads/2020/06/timecraft_canvas.png) 通过亚马逊土耳其机械公司进行的一项调查，对实验期间生成的延时视频进行了评估，158 名参与者被要求比较 Timecraft 视频和真实延时视频的真实性。结果是，参与者更喜欢真实的视频，但有一半时间会将 Timecraft 视频与实时延时视频混淆。

虽然可能还不完美，但它确实展示了如何使用 ML 来推断艺术作品是如何构建的，并以某种程度的准确性计算出各个步骤。

 [https://www.youtube.com/embed/iy1FCPQs4JI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iy1FCPQs4JI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

