# 二维步进电机

> 原文：<https://hackaday.com/2019/05/09/the-two-dimensional-stepper-motor/>

在 hackaday.io 上，在 hackaday 奖的深处，许多很酷的人都在探索在印刷电路板中放置线圈的可能性。从表面上看，这是有道理的:在 PCB 上画螺旋可以得到一个电磁铁。这让你可以做各种疯狂的事情。你可以用轨道做马达来制作微型磁悬浮列车模型。有人造了一个可穿戴的特斯拉线圈。

展示蚀刻在印刷电路板上的电机可能性的最新作品是[【bobricius】“微型机械手](https://hackaday.io/project/164507-2d-stepper-motor-etched-on-pcb-micro-manipulator)。这是一块 100 毫米见方的板，能够在表面移动一个小磁铁。重点是？好吧，如果你非要问这个问题，你真的永远不会明白。

这种步进电机的设计简单来说就是两圈导线，网格的 X 轴放在 PCB 的顶层铜层上，Y 轴放在底层铜层上。这些线圈中的每一个都有四个电极，它们直接插入标准的步进驱动器，所以要控制这个电路板，你只需要一个基本的 Arduino 和一个电机屏蔽。或者一个 RepRap 板，随便你挑，你可能有什么东西在垃圾抽屉里。

在该板的测试中，步进电机可以快速且高重复性地移动小型稀土磁体。至于这个 PCB 步进电机有什么用，非要问那个问题，你永远不知道。也是因为看起来很酷。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip) 

 [https://www.youtube.com/embed/EJZX66JzVDo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EJZX66JzVDo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

