# 追求更好的虚拟现实体验的触觉

> 原文：<https://hackaday.com/2020/02/12/in-pursuit-of-haptics-for-a-better-vr-experience/>

虚拟现实拥有沉浸式体验的承诺，可以满足我们的感官，达到与现实相当的水平。这个领域已经取得了很大的进展，但 Sarah Vollmer 提出了一个很好的观点，即目前使用的许多虚拟现实系统都很笨重，很难在人与人之间转移。

虽然耳机已经变得更小更轻，并且现在具有改进的运动跟踪和分辨率，但它们影响用户其他感官的能力却没有看到几乎相同的进步。触觉反馈系统需要赶上耳机，如何不引人注目地让用户在虚拟现实中感受模拟的身体接触是 Sarah 正在研究的领域，这是她博士工作的一部分。这是她 2019 年 Hackaday 超级大会演讲的主题，你可以在下面找到。

 [https://www.youtube.com/embed/aRkfiQZNx3I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aRkfiQZNx3I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



莎拉带来了她目前的原型系统中的一个，它充当多达八个不同致动器的中枢。用于传感器板的 PCB 包括两个切口，弹性带可以穿过这两个切口以将它们固定到手腕或身体的其他部分。每块电路板都支持偏心旋转质量(ERM)或线性谐振驱动器(LRA)，这两种类型的振动电机 ERM 可能让人联想到寻呼机电机，而 LRA 将不平衡的重量封装在一个圆盘中，该圆盘在与 PCB 垂直的轴上旋转。[开放式声控](http://opensoundcontrol.org/)用于向这些模块发送信号，与虚拟环境中的动作同步。

 [![Concept drawing for finger ring and bracelet haptic feedback system](img/3ec0087d1cbf716c8d3f964d7d1844c8.png "Sarah-Vollmer-haptic-ring-feedback")](https://hackaday.com/2020/02/12/in-pursuit-of-haptics-for-a-better-vr-experience/sarah-vollmer-haptic-ring-feedback/) Concept drawing for finger ring and bracelet haptic feedback system [![PCB for vibration motor modules](img/0b2f1b78049ba7c6448d9fa8792ad45c.png "Sarah-Vollmer-vibration-motor-pcb-design")](https://hackaday.com/2020/02/12/in-pursuit-of-haptics-for-a-better-vr-experience/sarah-vollmer-vibration-motor-pcb-design/) PCB for vibration motor modules

事情变得真正有趣的地方是莎拉为你的手和手腕设计的不引人注目的可穿戴设备的概念。目前的技术使用手套，但她在追求戒指和手镯。希望手腕和手指周围的戒指可以用于颗粒运动跟踪和触觉反馈。将空气或液体泵入材料内置的气囊中可以提供压力感，她甚至在研究使用直接电刺激的可能性。

不得不穿上笨重的设备与虚拟现实试图实现的效果相反。随着这项研究的继续，让系统既轻便又能紧密响应数字环境是让虚拟更真实的关键，也是我们所有人都可以期待的事情。