# Arduino 驾驶仿肺活量记录仪

> 原文：<https://hackaday.com/2021/12/10/arduino-drives-faux-spirograph/>

假期总是让我们想起小时候最喜欢的玩具。约翰尼·阿斯特罗，一套直立装置，当然还有一个肺活量描记器。[CraftDiaries]有一台 [Arduino 机器，它不完全是一台肺活量描记器](https://www.instructables.com/Arduino-Powered-Pattern-Making-Machine/)，但它确实让我们想起了一台。Arduino 驱动两个步进电机，连接到一支可以创建一些有趣图案的笔。

该建筑使用了一些激光切割的部件，但它们看起来并不像是用传统方法甚至 3D 打印很难制造的。作者甚至提到，如果你愿意，你可以用硬纸板或泡沫板来制作它们。

两个步进驱动器的电子器件非常简单。我们不禁认为，我们放在这里的一些旧的 3D 打印机主板可以很容易地处理这个问题。然而，在这个项目中，CPU 是一个普通的 UNO，带有 CNC 屏蔽来驱动电机。

当然，真正的诀窍是软件。显然，不同的模式来自于右侧运动神经和左侧运动神经的步伐延迟之间的关系。这背后肯定有一些数学计算，但模式肯定是漂亮的。

如果你喜欢看起来更像真实肺活量描记器的东西，[拿一袋乐高](https://hackaday.com/2017/06/29/making-spirographs-with-lego-and-math/)。或者试试[的自动相机](https://hackaday.com/2014/05/30/art-o-matic-is-spirographs-young-hip-offspring/)。

 [https://www.youtube.com/embed/bUO4_oLR0D0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bUO4_oLR0D0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

