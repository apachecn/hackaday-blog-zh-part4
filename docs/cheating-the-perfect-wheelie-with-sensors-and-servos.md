# 用传感器和伺服系统欺骗完美的轴距

> 原文：<https://hackaday.com/2018/09/24/cheating-the-perfect-wheelie-with-sensors-and-servos/>

每个人都记得他们第一次骑自行车的时候。这是一个令人振奋的时刻，当你找出正确的机制，在后轮轴上空保持平衡，成为街区最酷的孩子的光荣的几秒钟。然后重力开始起作用，你要么学会如何从后轮上把自行车卸下来，要么更有可能最终看着天空想知道你是如何站在地上的。

如果早就有这种前轮离地作弊装置的话，我们很多人都可以避免这种不光彩的命运。[汤姆·斯坦顿]对完美轮距的追求让他想到了这个设计，其实很简单。基本的想法是，当自行车达到一个人不敢超越的临界角度时，自动应用刹车。刹车使自行车减速，前轮放下，刹车释放，让你继续随着车轮跳动。该角度由一个连接到 Arduino 的加速度计读取，后制动杆由一个业余爱好伺服机构拉动。我们真的认为伺服将没有接近所需的扭矩，但事实上它做得很好。和大多数[Tom]的产品一样，他的设计过程也有很多断断续续的地方，但这都是学习的一部分。值得吗？我们将让[汤姆]在视频中讨论这个问题，但可以说的是，他在实地测试中从未撞到路面，尽管他在项目中表现得很熟练。

尽管如此，这是一个有趣的构建，并回避了系统如何改进的问题。这个自动平衡的机动独轮车中可能有一些线索吗？

 [https://www.youtube.com/embed/SpKltBb2n1M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SpKltBb2n1M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

