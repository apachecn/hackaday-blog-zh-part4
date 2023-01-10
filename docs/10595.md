# 绘画机械化大头针艺术

> 原文：<https://hackaday.com/2021/06/30/pinthing-mechanizes-pin-art/>

大头针艺术是那些如果触手可及就不能被单独留下的东西之一，不可避免地会留下手或脸的印记。[拥抱]也对它们着迷，所以他设计了 [PinThing](https://hackaday.io/project/180070-pinthing) ，一个机械化的别针艺术展示。

销针直径比标准销艺术大得多，但这是为了适应小型齿轮 DC 电机。每个销是一个短的 3D 打印的丝杠机构。电机由 Arduino Uno 顶部的一堆电机驱动器屏蔽驱动，Arduino Uno 使用 Firmata 通过串行从使用 Johnny-Five 库的 Node.js 应用程序接收指令。这可能是一个简单的 3×5 概念验证，但它可以用于从显示器到交互式桌面的任何东西。

像这样的像素化机械显示器，来自麻省理工学院的 [inFORM](https://hackaday.com/2013/11/07/inform-mits-morphing-table/) ，甚至是 [flip dot 显示器](https://hackaday.com/2021/05/29/3d-printed-flip-dots/)面临的挑战之一是致动器和驱动电子设备的成本。一个小的 10×10 阵列需要 100 个电机和驱动器，随着规模的扩大，这些数量会迅速增加，即使单个元件非常便宜。

如果你愿意牺牲每个像素的瞬时响应，可以使用一个[机械多路复用器](https://hackaday.com/2021/06/24/mechanically-multiplexed-flip-dot/)。它由显示器后面的某种移动托架和安装的致动器组成，因此每行只需要一个致动器，而不是每个引脚都需要。这也意味着销可以靠得更近，因为致动器可以在支架上交错排列。

PinThing 项目是 2021 年黑客日奖的[反思展示挑战赛的参赛作品，该奖项的](https://prize.supplyframe.com/)[决赛选手](https://hackaday.com/blog/)刚刚宣布。

 [https://www.youtube.com/embed/tx4W3ZDA_Vg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tx4W3ZDA_Vg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2021](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)