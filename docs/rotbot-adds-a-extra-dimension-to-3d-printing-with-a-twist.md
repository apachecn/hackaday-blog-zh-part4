# 机器人为 3D 打印增加了一个额外的维度

> 原文：<https://hackaday.com/2022/10/09/rotbot-adds-a-extra-dimension-to-3d-printing-with-a-twist/>

在我们看来，3D 打印机上的 Z 轴，或者几乎所有的数控机床，都没有得到充分利用。让 X 轴和 Y 轴一起工作来进行平滑的平面运动，而 Z 轴只是坐在那里等待它的重要时刻，最终只是将打印头和底座彼此移动几分之一毫米，这似乎不公平。Z 轴就不能多一点乐趣吗？

当然可以，虽然非平面 3D 打印并不是什么新鲜事，但 *CNC 厨房*的【Stefan】向我们展示了这个概念的文字扭曲，用[这个四轴非平面打印机](https://www.youtube.com/watch?v=7LRWuccMGjc)。出于显而易见的原因，它被称为“RotBot ”,它来自苏黎世应用科学大学，在那里[Michael Wüthrich]和他的同事们一直在尝试不同的切片策略，以使重叠打印更易于管理。硬件方面的东西实际上是非常直观的，尤其是如果你曾经见过一个工业水射流切割机的行动。他们修改了 Prusa 打印机，在打印头上增加了一个旋转延伸部分，将喷嘴与打印床成 45 度角。滑环连接加热器和风扇，并允许机头旋转 360 度，挤出机位于旋转机头上方。

在软件方面，苏黎世团队想出了一些聪明的变通办法，使用现成的切片机进行锥形切片。正如[Stefan]解释的那样，该团队使用了一个“预变形”步骤来扭曲模型，并欺骗切片器生成锥形 g 代码。g 代码然后以与预变形完全相反的过程被反向转换，然后被馈送到打印机。转换步骤是用一点 Python 代码完成的，结果非常简洁。看着四个轴同时一起工作是非常令人满意的，就像没有可见支撑手段的巨大突出物一样。

关于这个的学术论文可能值得一读，谢天谢地所有的代码都是开源的。我们很想看看这是否会在社区中流行起来。

 [https://www.youtube.com/embed/7LRWuccMGjc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7LRWuccMGjc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

