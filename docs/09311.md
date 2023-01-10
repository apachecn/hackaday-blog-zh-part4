# 树莓派 Pico 不能运行 Linux。但是可以运行 Fuzix。

> 原文：<https://hackaday.com/2021/02/19/the-raspberry-pi-pico-cant-run-linux-but-it-can-run-fuzix/>

就单板计算机而言，最大的分歧在于那些可以运行某种形式的基于 Linux 的发行版的计算机和那些不能运行的计算机。例如，Raspberry Pi Zero 是一个 Linux 板，而 Raspberry Pi Pico 的 RP2040 处理器缺乏运行每个人都喜欢的类似 UNIX 的操作系统所需的硬件。但这并不是说来自剑桥的新主板不能运行任何类似 UNIX 的操作系统，正如[David Given]用他的 Fuzix port 向我们展示的那样。

Fuzix 是一个类似 UNIX 的操作系统，面向能力较弱的处理器，更符合那些原始 UNIX 的精神，而不是基于现代 Linux 的发行版。它是受人尊敬的前 Linux 内核开发者和维护者艾伦·考克斯的作品，由一个内核、一个 C 编译器和一组核心的类 UNIX 应用程序组成。

RP2040 端口可能还需要一些工作才能被认为是稳定的。就目前而言，多任务支持还不太到位，NAND 闪存支持也不太好，但它确实支持 SD 卡，支持适当的 UNIX 文件系统和全套核心工具。也许最有趣的是，它只占用双核芯片的一个核心，留下了另一个核心和那些 Pio 用于其他目的的可能性。

这些年来，Fuzix 偶尔会出现在这里，但可能不像它应该出现的那样频繁。如果你想进一步了解 UNIX 的起源，[我们在 2019 年](https://hackaday.com/2019/11/05/will-the-real-unix-please-stand-up/)看了看。

标题:Michiel Henzler([CC BY-SA 4.0](https://commons.wikimedia.org/wiki/File:Raspberry_pi_pico_oben.jpg))。