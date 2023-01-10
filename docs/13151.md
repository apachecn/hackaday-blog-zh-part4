# 从头开始设计，全手工制作:模块化科尔曼 Z80 计算机

> 原文：<https://hackaday.com/2022/03/25/designed-from-scratch-and-fully-handmade-the-modular-coleman-z80-computer/>

虽然“我自己造了一台电脑”这句话对于外行人来说可能听起来印象深刻，但任何对现代计算机硬件感兴趣的人都知道，这其实没什么大不了的:买一个机箱，一个带 CPU 的主板，一些 RAM 和外围设备，你就差不多了。更令人印象深刻的是从头开始设计一个完整的计算机系统，就像约书亚·科尔曼在建造科尔曼 Z80 时所做的那样。

当我们说“从底层开始”时，我们是认真的:从系统总线开始的所有东西都是由[Joshua]自己手绘的。不过，它确实与现代个人电脑有一些共同之处:严格的模块化设计。有一个 Z80 CPU 板，一个 ROM 和 RAM 板，甚至有两个模块，你可以描述为视频卡和声卡。所有这些都建立在带有 40 针边缘连接器的原型板上，并连接到承载主系统总线的单个背板。

作为一个实验平台，科尔曼 Z80 具有许多功能，可以进行测试和调试，如可调时钟发生器和几个漂亮的老式 LED 显示器，显示主总线的状态。输入和输出主要通过一个串行链路和一个 16×2 的 LCD，但是[Joshua]已经在计划一个键盘接口和复合视频输出来给它一个合适的 80 年代家用电脑的氛围。该软件目前仅限于支持基本 I/O 命令的 ROM 监视器，但有了 256 KB 的 RAM，就有足够的潜力来编写有用的软件。

与设计本身一样令人印象深刻的是，这是[约书亚]的第一个电子设计项目；我们肯定见过更糟糕的第一个项目！这些年来，我们推出了几款很酷的自制 Z80 电脑，例如[一款超级简约的主板](https://hackaday.com/2020/07/17/a-z80-board-with-very-few-parts/)、[一款基于强大的 eZ80](https://hackaday.com/2020/02/23/a-z80-computer-at-the-next-level/) 的模块化系统，以及[这款可以放在 Altoids 罐子里的可爱小电脑](https://hackaday.com/2019/09/17/a-curiously-strong-z80-in-your-pocket/)。

 [https://www.youtube.com/embed/JD_VTdSlTJk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=3&wmode=transparent](https://www.youtube.com/embed/JD_VTdSlTJk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=3&wmode=transparent)

