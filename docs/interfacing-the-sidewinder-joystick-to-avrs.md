# Sidewinder 操纵杆与 AVRs 的接口

> 原文：<https://hackaday.com/2019/01/29/interfacing-the-sidewinder-joystick-to-avrs/>

Sidewinder 系列是微软从 20 世纪 90 年代开始生产的一系列游戏外设。在经历了一些最初的挫折后，在家用电脑市场处于不断变化的时期，从串行和并行等传统接口过渡到更现代的 USB，几款尖端的操纵杆问世了。在这一过渡时期，Sidewinder 游戏手柄使用了一种特殊的方法通过游戏端口接口进行数字通信，这种方法更典型地使用一种组合设备以模拟方式读取游戏手柄。[【MaZderMind】设法对该协议进行逆向工程，并在 AVR 微控制器上实现了该接口。](https://github.com/MaZderMind/SidewinderInterface)

该技术在[美国专利第 5628686 号](https://patents.google.com/patent/US5628686A/en)中有粗略描述，该专利讨论了用于与 Sidewinder 操纵杆双向通信的方法。[MaZderMind]发现专利文件与 Sidewinder Precision Pro 的通信方式并不完全一致，但它足够接近，可以对操作进行逆向工程。

该计划是使用老式操纵杆来控制四轴飞行器，因此该接口是在 AVR 上实现的，并且安装了图形 LCD 作为测试操作的显示器。[MaZderMind]还在示波器上捕捉数据，以详细显示操纵杆操作的古怪之处。

是的，完全可以使用更现代的带 USB 操纵杆的微控制器。然而，很少有符合老式 Sidewinder 硬件标准的，有时最好的工具就是您随身携带的工具。传统的单操纵杆是四轴飞行器控制的一种不同形式，但还有其他选择—[手势控制也是可能的。](https://hackaday.com/2014/10/16/controlling-a-quadcopter-with-gestures/)