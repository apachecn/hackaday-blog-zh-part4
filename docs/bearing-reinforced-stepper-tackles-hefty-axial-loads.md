# 轴承加强踏步机处理沉重的轴向负荷

> 原文：<https://hackaday.com/2019/08/11/bearing-reinforced-stepper-tackles-hefty-axial-loads/>

如今，在我们黑客中，给步进电机加载与其轴一致的力是很常见的——尤其是当我们将它们耦合到丝杠或蜗轮时。不幸的是，步进电机并不适合这种负载，用很大的力这样做会损坏电机。不过，不要害怕。如果您发现自己处于这种情况，[Voind Robot]为您提供了解决方案，一个非常简单但非常有效的升级，让您的步进器毫无问题地处理轴向负载。

在[Voind Robot]的案例中，他们从机器人手臂上的蜗轮传动开始。在这种情况下，移动机械臂可能会通过蜗杆向步进轴施加巨大的轴向载荷，多达 30 牛顿。这种负载很容易在短时间内破坏内部步进电机轴承，因此他们选择了一些双面加固。为了缓解这个问题，引进了两个推力轴承，轴的两侧各一个。这些推力轴承的工作是将力从轴上直接转移到电机外壳上，这是一个更加刚性的地方来施加这样的载荷。

[![](img/cab74df05f5cec79e36c236af237ac32.png)](https://hackaday.com/2019/08/11/bearing-reinforced-stepper-tackles-hefty-axial-loads/back_axial_loading/)[![](img/8c4c0596349848624b755db46574e3f5.png)](https://hackaday.com/2019/08/11/bearing-reinforced-stepper-tackles-hefty-axial-loads/front_axial_loading/)

这一招非常简单，实际上已经有五年多的历史了。尽管如此，对于今天任何考虑将丝杠耦合到 Z 轴步进电机的 3D 打印机制造商来说，它仍然具有不可思议的相关性。在那里，单个推力轴承可以消除任何轴向游隙，并导致整体刚性建设。我们喜欢这些简单的机器设计智慧。如果你正在寻找更多的打印机设计技巧，看看[Moritz 的] [Workhorse Printer 文章](https://hackaday.com/2016/07/06/build-a-3d-printer-workhorse/)就知道了。