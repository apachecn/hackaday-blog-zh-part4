# Gdbdiff:区别真实的 RP2040 MCU 和仿真的 MCU

> 原文：<https://hackaday.com/2021/06/03/gdbdiff-diff-ing-a-real-rp2040-mcu-against-an-emulated-mcu/>

开发 RP2040 仿真器，但逐个指令验证仿真器指令是一个缓慢而繁琐的过程，该怎么办？当然，如果你是[Uri Shaked]的话，会自动将其与真实硬件进行比较。这就是 [gdbdiff](https://hackaday.io/project/177082-raspberry-pi-pico-emulator/log/192865-gdbdiff-bug-squashing) 的目的。这个项目通过 OpenOCD 使用 GDB 远程串行协议来逐步运行测试固件。

在直播过程中(通过上面的链接链接的视频)，这允许[Uri]以这种方式在模拟器中找到一些指令错误。这些问题包括 APSR 注册中的错误旗帜和 LSRS 注册中的一个边缘案例。这个 gdbdiff livestream 是[整个系列](https://hackaday.io/project/177082-raspberry-pi-pico-emulator)实时编码会话的一部分，在此期间【Uri】从头开始编写一个 RP2040 仿真器。

我们为[Uri]的创造性思维喝彩，并认为这种方式的直播可能比纯手工进行指令级调试更具娱乐性:)