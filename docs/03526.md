# ESP32 使用这个 VGA GUI 库获得高级窗口应用程序

> 原文：<https://hackaday.com/2019/07/08/esp32-gets-advance-windowed-apps-using-this-vga-gui-library/>

今年 4 月，我们在 ESP32 上展示了[Fabrizio Di Vittorio]的 FabGL 库。该库允许 VGA 输出使用简单的基于电阻的 DAC (3 个电阻用于 8 种颜色；6 个电阻用于 64 种颜色)，包括 PS/2 鼠标和键盘输入功能、图形库和许多在 ESP32 上开发游戏可能需要的其他功能。现在，[增加了一个 GUI 接口库](https://github.com/fdivitto/FabGL)来简化应用程序开发。

当然，GUI 运行在 VGA 输出上。这个库包括了你所期望的最小化窗口 GUI，比如键盘和鼠标支持，带有常用的最小化/最大化/关闭控件的窗口，以及模态和消息对话框。对于输入控件，有标签、文本框、按钮、单选按钮、复选框、普通的和可编辑的组合框以及列表框——你知道，几乎是开发现代 GUI 应用程序所需的一切。所有代码都是开源的(GPL 3.0)并且在 [GitHub repo 中。](https://github.com/fdivitto/FabGL)

虽然最初的 FabGL 面向游戏开发，但这一新的 GUI 功能的加入开辟了一个新的应用领域。如果你想了解更多关于使用 FabGL 库的信息，你可以查看一下我们之前关于主要面向游戏的功能的报道。

休息之后，您可以在视频中看到新的 GUI 功能。

 [https://www.youtube.com/embed/84ytGdiOih0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/84ytGdiOih0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

