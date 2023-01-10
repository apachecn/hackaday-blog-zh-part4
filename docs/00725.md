# DIY Puff-Suck 界面旨在加快文本输入

> 原文：<https://hackaday.com/2018/09/25/diy-puff-suck-interface-aims-for-faster-text-input/>

喷吸(或吸吸)系统允许手臂很少或没有活动能力的人通过使用类似吸管的装置作为输入设备来更容易地与计算机交互。[Ana]告诉我们，这些设备通常用于输入文本的方式涉及基于屏幕的键盘；使用某种方法(操纵杆、鼠标模拟器、按钮或眼睛跟踪)将光标移动到一个字母上，通过啜饮或向试管中吹气来选择该字母。

[Ana]认为这种系统使用起来既有效又直观，但速度也有限，因为速度太快，一次只能选择一个字母。这导致了一种新方法的尝试；这需要用户做更多的工作，但是回报是更快的文本输入。用于快速文本输入的 [Puff-Suck 接口](https://hackaday.io/project/160107)将一个空心塑料盘和一个橡胶隔膜变成双极压力开关，能够检测三种状态:吸、喷和空闲。该装置的工作原理是在一个光阑的两侧各有一对红外发射器和接收器(上图中显示了其中的一半)。当空气被吹入或吸出该单元时，隔膜移动并物理地阻挡一个或另一个发射器-接收器对。产生的信号由附加的 Arduino 解释。

这如何实现更快的文本输入？抛弃通常的“屏幕键盘”界面，使用莫尔斯电码，用“噗”作为点，“吸”作为破折号。这个项目就像一种莫尔斯电码键盘。这确实需要用户的技巧，但是回报是更快的文本输入。这个想法入选了 2018 年 Hackaday 奖[人机界面挑战赛](https://hackaday.com/2018/09/05/twenty-projects-that-just-won-the-human-computer-interface-challenge/)部分的决赛！

对一些人来说，莫尔斯电码似乎是一种奇怪的回归，但不仅[Ana]的吸气开关的双极性质与莫尔斯电码输入拨片非常相似，而且它也很容易学习。莫尔斯电码远未消亡；我们有好几页的项目和新闻，显示它参与了从异想天开的项目到解决严肃的交流需求的所有事情。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)