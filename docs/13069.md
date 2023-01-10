# 模块化多输入宏键盘集成了鼠标和操纵杆

> 原文：<https://hackaday.com/2022/03/18/modular-multi-input-macro-keypad-integrates-mouse-and-joystick/>

虽然大多数计算机用户只使用键盘和鼠标，但高级用户通常有多个附加输入设备。游戏玩家使用游戏杆或专用鼠标，CAD 工程师使用专门的小工具来操作 3D 对象，而图形设计师可能需要可编程的宏按钮来自动执行各种任务。[Sascha Nitsch]不喜欢在他的桌子上堆满一大堆输入设备，因此决定将尽可能多的功能合并到 [CIMDIT 中:一个完全疯狂的多设备输入东西](https://contentnation.net/de/grumpydevelop/cimdit_1)。

组成 CIMDIT 的主要组件是一个 3 轴操纵杆模块，它可以兼作 3D CAD 鼠标，以及一组按钮、旋钮和滑块来实现各种功能。一个旋转编码器用于选择操作模式，而另外四个可用作可编程输入。一个小的有机发光二极管显示屏显示当前选择的模式，但也可以用来显示来自各种程序的通知。

Arduino Pro Micro 为 PC 提供 USB 接口，并读取各种输入单元。整个设计是模块化的，因此可以根据模拟和数字输入的任意组合进行定制。[Sascha]制作了一个整洁的 3D 打印外壳，以容纳 3 轴模块以及 26 个按钮、5 个旋转编码器和 1 个模拟滑块。PCB 的 KiCAD 文件和外壳的 FreeCAD 源代码可以在[【Sascha】的 Git repo](https://git.contentnation.net/grumpydevelop/cimdit) 上获得。

同样的事情也适用于驱动 CIMDIT 的软件，尽管向它添加功能可能会变得很棘手:[Sascha]必须执行一些严肃的代码优化，以将所有内容都放入 Arduino 的 32 kB 程序闪存中。Git repo 还包括一个方便的工具来创建要编程到控制器中的键映射，使您不必手工编写二进制文件。

喜欢宏键盘吗？用[手势检测](https://hackaday.com/2021/06/13/gesture-detecting-macro-keyboard-knows-what-you-want/)，一个[电子墨水显示屏](https://hackaday.com/2021/02/18/dynamic-macro-keyboard-controls-all-the-things/)或者简单的[漂亮的木键](https://hackaday.com/2021/05/21/custom-macro-keyboard-looks-good-in-wood/)来看看这些很酷的例子。