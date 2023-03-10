# 对抗图像识别的隐形斗篷

> 原文：<https://hackaday.com/2019/05/03/the-cloak-of-invisibility-against-image-recognition/>

对抗性攻击对于用于图像识别的深度网络世界来说并不新鲜。然而，随着深度学习研究的发展，更多的缺陷被发现。比利时鲁汶大学的团队展示了如何通过简单地使用[一张放在男人躯干附近的彩色照片，让基于卷积神经网络](https://arxiv.org/abs/1904.08653)的图像识别系统看不到他。

卷积神经网络或 CNN 是一类深度学习网络，它通过从更简单和更小的网络创建分层模式来减少要执行的计算数量。它们正在成为图像识别应用的标准，并且正在现场使用。在这篇新论文中，添加色标被视为通过添加干扰 CNN 计算的噪声来混淆图像检测器 YoLo(v2)。补丁不是随机的，可以使用出版物中定义的过程来识别。

这种攻击可以通过在 t 恤上印刷破坏性图案来实现，使其不被监控系统检测到。你可以阅读概述对抗性补丁生成的论文[ [PDF](https://arxiv.org/pdf/1904.08653.pdf) 。[图像识别伪装在谷歌成立之初](https://hackaday.com/2017/11/03/googles-inception-thinks-this-turtle-is-a-gun/)就已经被记录在案，我们希望在未来看到更多这样的黑客攻击。这是一个新世界，你的黑客生涯一如既往地丰富多彩。

 [https://www.youtube.com/embed/MIbFvK2S9g8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MIbFvK2S9g8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

