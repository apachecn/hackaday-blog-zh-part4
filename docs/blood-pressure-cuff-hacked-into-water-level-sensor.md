# 血压袖带侵入水位传感器

> 原文：<https://hackaday.com/2022/04/11/blood-pressure-cuff-hacked-into-water-level-sensor/>

我们经常写一个帖子，然后从评论中了解一些新的很酷的东西。同样的事情发生在安德烈亚斯发布了一个关于监测液位的视频。评论者告诉他，最好的液位传感器是一个被黑掉的血压计。他不知道，我们也不知道，直到我们看了他的视频。

众所周知，罐中顶部封闭而罐内开口的气密管将产生对应于罐中液位的压力。当您希望压力传感器远离储罐时，例如在封闭的建筑物中，这是一种常见的方法。那么，为什么要使用血压计呢？因为对该系统的一个常见的改进是首先使用泵对测量管加压，因此该系统可以容许小的泄漏。血压计有你需要的一切:一个泵、一个阀门和一个压力传感器。

为了得到准确的结果，你需要测量压差。根据您选择的类型，压力传感器可以测量表压、差压或绝对压力。[Andreas]拆开了一个便宜的血压袖带，里面有所有需要的部件。然而，像大多数廉价的消费设备一样，CPU 是一团神秘的环氧树脂。

由于 5V 电源，一些预建的传感器模块存在一些问题。最终，他使用了一种新的传感器，一种微控制器，然后使用了血压袖带中的泵和阀门。改变血压计的用途比从头开始建立一个密闭的系统更容易。

压力传感器通常只是老式气压计技术的复杂版本。像大多数事情一样，有许多方法可以测量液位，包括超声波、浮子、电容传感器、[，当然还有数学](https://hackaday.com/2019/11/11/water-flow-meter-knows-tank-level/)。

 [https://www.youtube.com/embed/h5Z5pAUJxC4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/h5Z5pAUJxC4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

