# 今天你终于学会了四元数

> 原文：<https://hackaday.com/2022/09/05/todays-the-day-you-finally-learn-quaternions/>

如果你曾经处理过轨道力学或复杂的计算机图形，你可能会遇到数学术语四元数。[Anyleaf]有一个关于这个数学概念的实际使用的指南，它更注重实用性而不是理论。我们喜欢！

四元数是在 3D 空间中模拟旋转的至少两种方式之一。大多数人都熟悉经典的欧拉角，包括偏航、俯仰和滚转。然而，这种方法容易产生一些歧义，换句话说，从一个欧拉状态到另一个状态有多种方法，并且所有方法都同样有效。此外，在两个轴平行的情况下，欧拉角容易发生万向节锁，因此不会对对象的方向产生不同的影响。有几种方法可以解决这个问题，包括使用四元数。

如果你认为万向节锁不是问题，不要忘记阿波罗 IMU 有这个问题，因为他们使用三个而不是四个万向节。系统会检测到它处于万向锁定状态，需要人工干预。这促使[迈克·科林斯]和[开玩笑说:“圣诞节送我第四个万向节怎么样？”](https://apollo11space.com/apollo-and-gimbal-lock/)

当然，你可以在欧拉角和四元数之间转换，这取决于所涉及的模糊性。但是，关于从四元数转换的部分被标记为将来的工作，所以您可能需要更多的资源来填补空白。如果你想了解更多细节，[Anyleaf]推荐了一个来自[【3 blue 1 brown】和【Ben Eater】](https://eater.net/quaternions)的优秀页面，其中有可探索的视频(标题图片来自其中一个视频)和来自魏茨曼科学研究所的 PDF 教程[。](https://www.weizmann.ac.il/sci-tea/benari/sites/sci-tea.benari/files/uploads/softwareAndLearningMaterials/quaternion-tutorial-2-0-1.pdf)

老实说，我们知道不是每个人都喜欢数学，这是真的——尤其是今天——你可以不钻研数学而做很多事情。但是，如果你知道事情背后的数学原理，这通常会使事情变得更容易，有时甚至是可能的。它就像汇编语言。现在你可能不需要知道它，但是如果你知道它，它有时会以奇怪和意想不到的方式帮助你。那么，为什么不温习一下微积分或者像 T2 拉普拉斯变换这样的高级课题呢？