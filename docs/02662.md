# 台式车床得到一个电子丝杠改造

> 原文：<https://hackaday.com/2019/04/17/benchtop-lathe-gets-an-electronic-leadscrew-makeover/>

机床之王是车床，如果国王有心的话，大概就是丝杠了。这是允许螺纹操作的钻头，可以说是车床能够处理的最重要的工作。实际上，这是一个简单的概念——丝杠通过齿轮与主轴机械连接，这样刀具在旋转时就可以沿着工件的长轴移动，从而切割出所需螺距的螺纹。

但是在概念上简单的事情在现实中可能会很复杂。正如[Clough42]所指出的，大多数车床通过一系列复杂的齿轮将丝杠连接到主轴驱动装置，这些齿轮需要换进换出以适应不同的螺距，这使得从英制到公制本身就像一个完整的球。所以他开始为他的车床制造电子丝杠。这个想法是放弃齿轮系，直接用高质量的步进电机驱动丝杠。这听起来很简单，但请记住，刀具的平移需要与主轴的旋转完全同步，才能实现螺纹加工。这将通过耦合到主轴的工业级正交编码器来实现，它将告诉 TI LaunchPad 上运行的软件旋转步进器的速度和方向，以控制螺纹旋向。下面的视频详细介绍了微控制器上的实时操作系统，以及对所有要使用的硬件的测试。

在这一点上，这只是一个概念验证，但是我们期待这个系列的其余部分。同时，[【奎因邓基】关于选择车床的优秀系列](https://hackaday.com/2018/02/21/the-king-of-machine-tools/)应该会让你坚持下去。

 [https://www.youtube.com/embed/FTs9GygRQ-U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FTs9GygRQ-U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

