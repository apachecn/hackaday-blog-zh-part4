# 无声步进电机使机电时钟适合客厅

> 原文：<https://hackaday.com/2022/03/10/silent-stepper-motors-make-electromechanical-clock-fit-for-a-living-room/>

大型机械七段显示器有一种在电子屏幕上看不到的存在感。这部分来自于他们在每次转换时发出的相当令人满意的咔哒咔哒声。不幸的是，这样的噪音很快就会在你的客厅里变得令人讨厌；[David McDaid]因此设计了一款静音的机电七段钟,它具有机械显示的所有功能，但没有伴随的声音。

正如[David]在一篇非常全面的博客文章中描述的那样，这种无声操作的关键是使用步进电机而不是伺服电机，并使用 TMC2208 步进电机驱动器来驱动它们。这种芯片有一种独特的调节电流的方法，不会在电机内部引入机械振动。与伺服系统相比，一个缺点是所需的控制线数量:每个电机有四条线，当你试图组装四个七段显示器时，电缆管理就成了一个问题。

时钟是建立在一大块 MDF 上的，所有 28 个电机在前面，电子设备在后面。定制的安装支架和显示部分都是 3D 打印的，而四个大型 PCB 固定着步进电机驱动器和连接器，将它们连接到电机上。额外的 PCB 拥有一个运行整个节目的 Arduino Mega 2560，一个用于精确计时的 DS3231 实时时钟，以及一个管理显示器消耗的 40 多瓦功率的电源。

除了显示当前时间，时钟还包括一个闹钟，一条 LED 灯和一个“随机单词生成器”:按下一个按钮，显示器将显示一个随机的四个字母的单词。我们不确定该特性的确切用例，但它是对一个非常简洁的构建的一个简洁的补充。如果你喜欢机械七段钟，你很幸运:我们有基于单个步进电机的[、](https://hackaday.com/2021/11/13/a-one-servo-mechanical-seven-segment-display/)[充满木制齿轮的](https://hackaday.com/2021/10/25/mesmerizing-mechanical-seven-segment-display/)、[有突出段的](https://hackaday.com/2020/07/27/mechanical-seven-segment-display-really-sticks-out-from-the-pack/)和[有许多伺服系统的](https://hackaday.com/2021/08/11/a-whole-lot-of-stepper-motors-make-the-most-graceful-7-segment-displays/)。

[![An electromechanical wall clock that shows random words when a button is pressed](img/30039260ffabe108eb35ea5e5b5331d3.png)](https://hackaday.com/wp-content/uploads/2022/03/word_gen.webp)