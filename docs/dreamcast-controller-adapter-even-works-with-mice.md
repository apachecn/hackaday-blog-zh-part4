# Dreamcast 控制器适配器甚至适用于鼠标

> 原文：<https://hackaday.com/2021/03/16/dreamcast-controller-adapter-even-works-with-mice/>

PC 游戏玩家受益于为满足其游戏乐趣而构建的广泛外设生态系统。另外，如果有什么东西不能在这个平台上工作，可能有人已经在卖它的适配器了。游戏机玩家就没那么幸运了，绝大多数人坚持使用出厂标准控制器。[megavolt85]却不在其中，[并为世嘉 Dreamcast 安装了多适配器。](https://www.dreamcast-talk.com/forum/viewtopic.php?t=13058)

该适配器允许玩家在 Dreamcast 上使用各种各样的控制器。有对 PS1 和 PS2 控制器的支持，包括振动支持，以及 MegaDrive 和土星垫。PS/2 鼠标和键盘也可以使用，并且最多可以连接 16 个 vmu。该适配器使用 STM32F103C8T6 微控制器，运行速度高达 72MHz，使其有足够的咕噜声来模拟 Dreamcast 的 Maple 控制器接口。

我们也看到了 Dreamcast 控制器总线的其他黑客攻击；这个定制控制器在 Raspberry Pi Pico 上实现了接口。如果你一直在制作自己的梦幻组合，一定要给我们写信！