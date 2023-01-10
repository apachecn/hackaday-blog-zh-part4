# 非常规无人机使用气体推进器进行控制

> 原文：<https://hackaday.com/2019/06/08/unconventional-drone-uses-gas-thrusters-for-control/>

你不得不佩服[汤姆·斯坦顿]——他真的有创新思维。也可能在大气层之外，也就是说:我们展示[他的反作用控制气体推进器控制的无人驾驶飞机](https://www.youtube.com/watch?v=XpA6qpNlNOE)。

在任何人过于兴奋之前，[汤姆]不是在真空中制造无人机，尽管我们肯定可以看到这种设备的使用案例。这更像是一件混合的事情，反向旋转的推进器安装在位于中央的导管中，提供升力和偏航控制。旁边是一个三角形框架，支撑着三个两升的汽水瓶储气罐，每个储气罐在三角形的每个顶点都提供一个向下燃烧的喷嘴。电磁阀控制压缩空气从瓶子到喷嘴的流动，提供推力以稳定滚转和俯仰轴。由于没有很多现成的飞行控制系统用于反作用控制，[汤姆]不得不临时准备推进器控制；Arduino 会观察通常发送给无人机马达的油门信号，并在它们达到预设阈值时触发螺线管。这需要一些调整，但[汤姆]最终能够得到一个稳定的，不受束缚的悬停。他是对的——只要主发动机关闭，RCS 喷气机开火时听起来确实很惊人。

这看起来似乎有很大的潜力，我们希望看到它得到更多的发展。这让我们想起了这个涵道螺旋桨无人机，这是另一个将传统无人机控制概念延伸到极限的伟大例子。

 [https://www.youtube.com/embed/XpA6qpNlNOE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XpA6qpNlNOE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

