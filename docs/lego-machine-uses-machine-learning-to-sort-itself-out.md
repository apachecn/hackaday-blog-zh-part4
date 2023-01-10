# 乐高机器使用机器学习来整理自己

> 原文：<https://hackaday.com/2019/12/16/lego-machine-uses-machine-learning-to-sort-itself-out/>

在我们看来，一个正常生活的童年的主要证据是一个巨大的盒子，里面装着每一个可以想象的乐高积木，从简单的砖块到大梁和齿轮，所有的玩具都有一个小镇的价值。积累一个最好用磅来衡量的乐高收藏品需要多年的生日和圣诞节，但就像任何值得做的事情一样，这是值得做的。

但是如何处理这样的收藏呢？翻箱倒柜地寻找合适的物品可能会令人沮丧，而用手动分拣将混乱变得有条不紊是非常不切实际的。用乐高制成的[机器视觉乐高分类器来处理这些砖块怎么样？](https://towardsdatascience.com/a-high-speed-computer-vision-pipeline-for-the-universal-lego-sorting-machine-253f5a690ef4)

[丹尼尔·韦斯特]的方法并不新鲜——我们以前甚至展示过[积木式乐高分拣机](https://hackaday.com/2011/04/08/nxt-machine-sorts-lego-blocks-automatically/)——但它的架构给我们留下了深刻的印象。第一，机械系统很神奇。它使用一系列传送带从料斗中运送砖块，并在运送过程中对水流进行风选。最后一步是振动进料器，每次将一块放在传送带上。这些通过连接到 Raspberry Pi 的摄像头，OpenCV 从视频流中进行背景减法，对零件应用边界框，并通过卷积神经网络(CNN)运行图像，该网络已经在每个乐高零件的数据库中进行了训练。然后，伺服控制门将零件送入 18 个箱子中的一个。请观看下面的视频。

我们必须承认，我们不确定排序标准是什么，因为有些箱看起来几乎和输入混合一样混乱。尽管如此，我们欣赏精细的工程，并奖励所有乐高的优点额外的风格点。

 [https://www.youtube.com/embed/04JkdHEX3Yk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/04JkdHEX3Yk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[via [The Verge](https://www.theverge.com/2019/12/11/21011792/lego-ai-universal-sorting-machine)

感谢[我妻子]的提示。