# ESP32 虚拟机让您随时更改程序

> 原文：<https://hackaday.com/2022/02/27/esp32-virtual-machine-lets-you-change-programs-on-the-fly/>

通常，对微控制器进行重新编程需要将它置于复位状态，刷新代码，然后让它重新启动。它通常包括完全关闭芯片。然而，[bor0]已经建立了一个运行在 ESP32 上的虚拟机，[允许进行动态程序更新。](https://github.com/bor0/evm-esp32)

该代码的灵感来自于 [CHIP-8，](https://hackaday.com/2020/12/07/inside-chip-8/)一种相对古老的解释器，有一些游戏应用。[bor0]已经创建了一个模拟 CHIP-8 的虚拟机，并在这里重新利用它，取出与游戏相关的绘图指令，并用控制 IO 引脚的指令来替换它们。寄存器也改为 16 位，以增加灵活性和裕量。

对于大多数人来说，这可能不是即时的突破性应用程序，但这是一种不同的使用和编程 ESP32 的方式，非常简洁。

众所周知，ESP32 也是一款功能强大的芯片—[,它是一款出色的 8 位仿真器。](https://hackaday.com/2020/06/09/run-your-favorite-8-bit-games-on-an-esp32/)请在评论中说出您对 ESP32 VM 杀手级应用的想法！

【感谢 satancete 的提示！]