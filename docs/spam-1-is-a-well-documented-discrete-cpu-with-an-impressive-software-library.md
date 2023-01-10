# SPAM-1 是一个有据可查的独立 CPU，具有令人印象深刻的软件库

> 原文：<https://hackaday.com/2021/11/06/spam-1-is-a-well-documented-discrete-cpu-with-an-impressive-software-library/>

在 Hackaday，我们喜欢那些被很好地记录下来的项目，以至于你可以花上几天的时间来阅读设计师所取得的成就。[约翰·朗尼根]在设计 SPAM-1 时没有让人失望，这是一个由离散逻辑门构建的 8 位 CPU。他的详细日志包含了丰富的信息，如设计操作码、优化程序计数器逻辑、运行数字仿真，以及他对微码设计的想法。对于初学者来说，它的庞大体积可能有点令人不快，所以最好从描述架构并详细介绍几个子模块的[视频系列](https://www.youtube.com/playlist?list=PLdLE_IdL0sqyAxmmHNbp0Q6dVWFVW8zQQ)开始。

自从[John]第一次开始这个项目以来，设计已经发生了一些变化，因为他决定添加越来越多的功能，但最终的结果是一个经过深思熟虑的架构，它保持了分立硬件所需的简单性，但仍有足够的功能让经验丰富的 CPU 爱好者感兴趣。指令大小相当大(48 位)，以更大的代码大小为代价来简化指令解码。条件跳转指令不存在；相反，所有指令都有一个可选的控制标志来使它们有条件，这是一个受 ARM 指令集启发的功能。

一旦设计足够成熟，[John]在 Verilog 中对整个设计进行建模，并模拟他的设计，以验证正确的操作并检查时序，估计其工作频率最高可达 5 MHz 左右。来自 74xx 系列的一大堆试验板和 DIP 芯片使设计变得栩栩如生。

不满足于简单地在硬件中设计、模拟和实现定制的 CPU，[John]还在软件方面花费了大量的精力，为 SPAM-1 平台编写了汇编程序，甚至是类似 C 的编译器。如果这还不够的话，他还为经典的 CHIP-8 语言添加了一个模拟器，允许它运行现有的程序，如 Pong 和 Tetris。所有这些软件的输入和输出主要是通过 UART 连接到 PC。VGA 接口仍然在[约翰]的任务清单上，但他确实制作了一个适配器，将传统的 NES 控制器连接到系统上。

SPAM-1 是我们在这里看到的一长串离散逻辑 CPU 的一个有价值的补充，如[这台运行类 UNIX 操作系统的试验板计算机](https://hackaday.com/2021/03/09/full-diy-a-unix-clone-on-ttl/)或[这台极简的](https://hackaday.com/2019/06/23/a-ttl-cpu-minimising-its-chip-count/)。如果你想看到一台实现现有指令集的计算机，试试这台[自制 RISC-V 计算机](https://hackaday.com/2021/04/13/homebrew-risc-v-computer-has-beauty-and-brains/)。

 [https://www.youtube.com/embed/kNQrdY7vQEo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kNQrdY7vQEo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

