# 奇怪的输入和特殊的外设:GameBug 把你的试验板变成了游戏控制台

> 原文：<https://hackaday.com/2022/06/05/odd-inputs-and-peculiar-peripherals-the-gamebug-turns-your-breadboard-into-a-game-console/>

有什么比玩电子游戏更有趣？当然是设计你自己的视频游戏硬件！如果你跟随这些页面足够长的时间，你会看到几十个家酿硬件的伟大例子，也许会启发你自己尝试这样一个项目。这通常始于将基本位组装到无焊试验板上，这对于编程来说很好，但对于测试来说不太好:将按钮挤压到试验板上可以进行基本调试，但不是非常用户友好或可靠。在[【Dimitar】的 GameBug 中可以找到一个更好的解决方案:一套兼容试验板的类似游戏手柄的控制器](https://hackaday.io/project/184026-gamebug)。

GameBug 的设计非常简单:一个微型模拟操纵杆，四个排列成菱形的按钮，一个肩部按钮和两个滑动开关位于一个整洁的紫色 PCB 上。底部是两排引脚头，确保与无焊试验板紧密贴合。甚至还有一个小型振动电机用于触觉反馈。

集成的读出电子设备简化了与 GameBug 的接口。基于施密特触发器的去抖电路确保所有按钮发出干净的信号，而电机驱动芯片为触觉反馈系统提供稳定的电流。RGB LED 可以用作另一种用户反馈设备，或者仅仅用于装饰照明。

所有的设计文件都可以在[Dimitar]的[GitHub 页面](https://github.com/MitkoDyakov/GameBug)上找到，还有一个 Arduino 草图可以帮助你尝试 GameBug 的功能。拥有一个合适的游戏手柄可能会在基于试验板的游戏系统中派上用场，如[小鸭子狩猎](https://hackaday.com/2020/03/08/tiny-duck-hunt-looks-like-big-fun/)或这个[令人印象深刻的一堆电线组成的 Colecovision](https://hackaday.com/2016/03/07/breadboard-colecovision/) 。

[![A pair of purple PCB-based game controllers](img/c86ce13b5f08e187f14811dad178f552.png)](https://hackaday.com/wp-content/uploads/2022/06/GameBug-Close-up.jpg)

[![Odd Inputs and Peculiar Peripherals Contest](img/4c1d0cbefc0219866bf706dbbac40818.png)](https://hackaday.io/contest/185414-odd-inputs-and-peculiar-peripherals)