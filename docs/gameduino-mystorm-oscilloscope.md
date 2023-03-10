# Gameduino + Mystorm =示波器！

> 原文：<https://hackaday.com/2018/08/04/gameduino-mystorm-oscilloscope/>

自从像最初的 Game Boy 这样的系统推出以来，我们中肯定有不止一个人看到了这些手持平台，并认为“你可以用它来制作一个非常小巧的示波器！”但是商业系统是闭源的、封闭的、专有的，所以在很多情况下，创造这样一个设备是不容易的。

不过幸运的是，现在已经有了非常方便的手持游戏平台，Gameduino 系列电路板的创造者[James Bowman]写信告诉我们关于[Lawrie Griffiths]为 Gameduino 3 创建的示波器项目[。它使用 Mystorm FPGA 板和 AN108 模拟板，虽然繁重的采集工作由 FPGA 处理，但它留给 Mystorm 的 STM32 与 Gameduino 对话。有一些初期问题，如 Gameduino 抱怨数据输入太快，但结果是一个有效的 8 MHz 带宽的触摸屏界面。然而，他也承认目前的界面有点复杂。](https://forum.mystorm.uk/t/gameduino-oscilloscope/447)[所有的代码都可以通过 GitHub](https://github.com/lawrie/verilog_examples/blob/master/fpga/oscilloscope/oscilloscope/oscilloscope.ino) 获得，所以如果你想自己探索这条特殊的途径，你可以。

多年来，我的风暴已经不止一次在这里出现，我们相信我们会看到更多。我们看到[模仿一个小的有机发光二极管显示器](https://hackaday.com/2018/03/11/fpga-magic-puts-little-embedded-screens-up-on-the-big-screen/)将 Arduboy 图形放在大屏幕上，例如，实现[一个完整的 Acorn BBC 微型家用电脑](https://hackaday.com/2017/09/24/a-very-2017-take-on-a-bbc-micro/)。