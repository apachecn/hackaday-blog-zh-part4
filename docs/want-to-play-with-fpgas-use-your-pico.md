# 想玩 FPGAs？用你的对讲机。

> 原文：<https://hackaday.com/2022/12/31/want-to-play-with-fpgas-use-your-pico/>

曾经想玩 FPGA，但没有硬件？现在，如果你有一个永远丰富的 Pi Picos，你可以开始玩 Verilog 而不用 FPGA 板。由[tvlad1234]开发的 FakePGA 项目基于 Verilator 工具包，为您提供了一种将 Verilog 编译成 RP2040 的 C++的方法。FakePGA 甚至集成了 RP2040 GPIOs，因此它们可以作为模拟 gpio 的数字引脚，这是计算机辅助 FPGA 代码模拟的一大进步

[tvlad1234]提供了在 Linux 上进行设置的说明——Windows 虽然未经测试，但理论上可以通过 WSL 运行。最大时钟速度是 5k Hz——不多，但比没有任何硬件测试要好得多。你想要的一切都在 GitHub repo 中——安装说明、Verilog 代码要求和一些需要记住的配置警告。

我们涵盖了很多使用 FPGAs 来仿真各种硬件的项目，从 [ISA 卡](https://hackaday.com/2022/11/13/emulate-any-isa-card-with-a-raspberry-pi-and-an-fpga/)到[一个完整的游戏机](https://hackaday.com/2021/09/07/gateboy-is-a-game-boy-emulated-at-gate-level/)。[FPGA 上的 CPU 仿真](https://hackaday.com/2019/11/19/emulating-risc-v-on-an-fpga/)基本上是标准——这只是利用 FPGA 提供的那种能力很容易做到的事情。反方向仿真并不常见，不过，我们已经看到[FPGA 与](https://hackaday.com/2019/06/28/yo-dawg-i-heard-you-like-fpgas/)FPGA 进行仿真，所以这可能是不可避免的。当然，如果你既没有 Pico 也没有 FPGA，总会有基于浏览器的仿真器。

我们感谢[兰迪·格伦]与我们分享这些！

 [https://www.youtube.com/embed/LUlhllMtDoI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LUlhllMtDoI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

