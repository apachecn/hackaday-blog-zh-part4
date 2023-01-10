# 印度 RISC-V 芯片是团队第三个成功的芯片

> 原文：<https://hackaday.com/2020/10/03/indian-risc-v-chip-is-teams-third-successful-chip/>

曾经有一段时间，创造一个新的集成电路是一个非常昂贵的命题。尽管这还不是一笔小数目，但定制芯片对老练的实验者和团体来说是触手可及的。作为证据，[看看 SHAKTI 集团的 Moushik CPU](https://abopen.com/news/shakti-announces-third-silicon-success-with-the-arduino-compatible-moushik/)。这是该集团的第三次成功流片，是一个开源的片上 RISC-V 系统。

该芯片采用 180 纳米工艺，有 103 个 I/O 引脚。CPU 运行速度约为 100 MHz，系统包括 SDRAM 控制器、模数转换和常用外设。大约 25 平方毫米的模具容纳了近 65 万个门。

这是 2018 年基于 RISC-V 构建自主芯片的同一个小组，与印度马德拉斯理工学院有关联。我们不清楚复制设计所需的所有东西是否都在 [git 库](https://gitlab.com/shaktiproject/cores/shakti-soc/-/blob/master/README.rst)中，但由于该项目是开源的，我们认为是。

仔细想想，收音机从高度专业化的设备变成了近乎一次性的消费品。计算器和电脑也是如此。用 FPGAs 开发一年比一年便宜，一年比一年容易。按照这种速度，不难想象，用不了多久，定制芯片就会像订购 PCB 一样简单——这在以前是一件非常棘手的事情。

当然，我们经常看到基于 FPGA 的 RISC-V。虽然我们钦佩[山姆·泽洛夫的][T2 的]工作，但我们不认为他将 65 万门打包成那个尺寸。反正还没有。

 [https://www.youtube.com/embed/KpRJe915-9I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KpRJe915-9I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

