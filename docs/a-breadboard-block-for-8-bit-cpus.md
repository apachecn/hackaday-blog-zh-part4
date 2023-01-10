# 用于 8 位 CPU 的试验板模块

> 原文：<https://hackaday.com/2020/10/12/a-breadboard-block-for-8-bit-cpus/>

试验板 CPU 是一种奇妙的学习体验，需要认真的投入和耐心。偶尔，CPU 制造商会避开他们的试验板，将他们的设计制作到 PCB 上。但是这剥夺了试验板 CPU 提供的灵活性和一些学习机会。就像大多数 8 位试验板 CPU 使用内存、总线、IO 控制器、rom 和一些其他无源组件一样,[c0pperdragon]在项目之间做着同样的重复布线。

采取一种折中的方法，[c0pperdragon]建造了一个 [PCB，可以用作他的定制 CPU](https://github.com/c0pperdragon/ByteMachine)的构建模块，他们将其命名为“ByteMachine”。单行 34 引脚提供电源、时钟、复位、19 条地址总线、8 条数据总线和一个 ROM 选择器。这意味着 CPU 可以安装在一个试验板上，运行速度更快，因为试验板的阻抗对电路的影响更小。ByteMachine 有 512 KB 的 RAM 和 512 KB 的 ROM，在一个便于重新编程的 ZIF 插座中，有足够的空间。

一个缺点是缺乏 IO。没有专用的地址空间，因为这需要 RAM 和 CPU 之间的解码逻辑。[C0pperdragon]添加了一个由 74 系列逻辑 ic 提供的简单 8 位输出寄存器。数据显示在 8 个红色发光二极管上，可以通过引脚访问。输入以类似的方式完成，仅提供 8 位数字输入。

【C0pperdragon】用 ByteMachine 建造了 [65C02](https://github.com/c0pperdragon/ByteMachine/blob/master/65c02) 、 [65C816](https://github.com/c0pperdragon/ByteMachine/blob/master/65c816) 、 [Z84C00](https://github.com/c0pperdragon/ByteMachine/blob/master/z84c00) 和 [i8088](https://github.com/c0pperdragon/ByteMachine/blob/master/i8088) 。每一个都在 GitHub 上记录了令人难以置信的图表、图片和测试程序。下次你想在试验板上构建 CPU 的时候，也许可以从 ByteMachine 开始。在某些方面，它可能会改善你的学习体验，因为它使我们在其他项目中看到的令人难以置信的大量电线变得更容易管理。

感谢[赖因哈德格拉夫]发送这一个！