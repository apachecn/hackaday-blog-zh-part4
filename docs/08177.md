# 电表上的时钟

> 原文：<https://hackaday.com/2020/10/29/a-clock-from-an-electricity-meter/>

世界各地的电力公司一直在将其电表从带有独特转盘的感应模拟式电表过渡到数字“智能”电表，这种电表不太美观，但对电力公司和客户都有很多好处。首先，抄表员不需要每个月访问每一个电表，因为它们都联网在一起，可以远程下载使用数据。另一方面，这意味着许多模拟仪表现在可用于项目，如【蒙他】的[这个时钟。](https://www.youtube.com/watch?v=JhDgKrleW2Q)

模拟电表的工作原理是将任何用电通过一个小型感应电动机，电动机的转速与通过它的能量成正比。这个小马达通过齿轮转动一组刻度盘，以记录家庭或企业的能源使用情况。为了运行时钟，[蒙他]将一个带有定制传动装置的步进电机连接到钟面的表盘上，因为不可能让感应电机旋转得足够快来驱动表盘。Arduino 控制步进电机，但不能简单地以线性方式驱动系统，因为它需要每小时跳过一大部分“分钟”表盘。类似的问题也出现在“小时”刻度盘上，但是一点额外的代码也解决了这个问题。

一旦真正的时钟完成后，[蒙他]对它进行一些收尾工作，如在玻璃罩上安装背光，并安装第二个电机来旋转感应电机轮，使仪表看起来像在运转。这是一个精心打造的建筑，很好地利用了一些古董硬件，就像我们看到的他的另一个建筑一样[从斯特林发动机](https://hackaday.com/2017/04/19/ethanol-powered-arduinos/)中获取能量。

 [https://www.youtube.com/embed/JhDgKrleW2Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JhDgKrleW2Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

