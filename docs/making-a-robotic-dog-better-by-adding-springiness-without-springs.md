# 在没有弹簧的情况下增加弹性，让机器狗变得更好

> 原文：<https://hackaday.com/2019/11/08/making-a-robotic-dog-better-by-adding-springiness-without-springs/>

让有腿机器人保持直立，尤其是四足动物或两足动物，可能是一项具有挑战性的任务。为了试验不同的方法，[詹姆斯·布鲁顿]建造了机器狗测试平台，并正在玩“[动态顺从模拟弹簧](https://youtu.be/bHCzrDr-t3w)”，或者换句话说，使用马达来充当弹簧和阻尼器..

当机器人腿保持僵硬时，由于机器人的突然不稳定运动，它们往往会降低平台的稳定性，特别是在不平坦的表面上。对于可反向驱动的接头布置，[James]在电机上使用有限的保持电流，并且使用编码器监控电机轴的位置。当一条腿受到阻力时，会有一些“弹性”，然后马达会更慢地将它返回到预定位置。在机器人顶部使用 IMU，它可以检测何时开始向一侧倾斜，然后暂时软化另一侧以平衡机器人。

这在腿式机器人中是一种很常见的技术，但是[詹姆斯]很好地解释了它是如何工作的。他希望利用从测试平台中学到的经验来改进或重新设计他已经令人印象深刻的 OpenDog。

最近我们在 Hackaday 上看到了一些四足机器人。包括 Boston Dynamics 非常昂贵的 [Spot](https://hackaday.com/2019/09/25/ask-hackaday-what-good-is-a-robot-dog/) 以及一只低成本的机器狗，让它的[老大哥们为他们的钱而战](https://hackaday.com/2019/09/22/watch-legged-robot-run-circles-around-its-bigger-brethren/)，并在这个过程中做一些[后空翻](https://hackaday.com/2019/05/29/robotic-cheetah-teaches-a-motors-class/)。休息之后看看詹姆斯的视频。

 [https://www.youtube.com/embed/bHCzrDr-t3w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bHCzrDr-t3w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

