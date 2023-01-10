# 这个 3D 打印的大游戏男孩实际上运行 MacOS

> 原文：<https://hackaday.com/2022/04/03/this-big-3d-printed-game-boy-actually-runs-macos/>

虽然如今手机游戏已经在很大程度上转移到了智能手机上，但经典的 Game Boy 仍然是复古爱好者非常受欢迎的平台，这在很大程度上归功于其庞大的优质游戏库。最初的 Game Boy 硬件非常防弹，但今天感觉有点过时，因为它缺乏大型背光显示屏或可充电电池等现代便利设施。

[iketsj]想要对 Game Boy 的设计进行现代改造，并设计了一个由现代单板计算机驱动的经典掌上电脑的 3D 打印超大副本。大多数人会选择像运行 Linux 的 Raspberry Pi 这样显而易见的东西，但不是[Ike]:他决定选择 LattePanda Alpha 板，并在上面运行 macOS Monterey。这使得它成为了一款 Hackintosh，也可能是最后一款，因为苹果正忙于将其所有产品移植到自己的专有 CPU 上。

LattePanda 的主板上还集成了一个 Arduino，用于读取 Game Boy 的按钮以及电阻式触摸屏。它通过模拟鼠标移动和按键的 Python 脚本与 macOS 系统进行通信。遗憾的是，触摸功能不起作用，因为[Ike]在试图缩小显示模块时意外损坏了触摸感应系统。不过，运行 Game Boy 模拟器时，七个按钮已经足够了，还有一个 USB 连接器可用于连接键盘、鼠标或显示器等外围设备。

这些年来，我们已经看到了几个伟大的 Game Boy 项目:[一些由黄铜制成](https://hackaday.com/2021/01/21/game-boy-replica-built-in-brass/)，[一些非常宽的](https://hackaday.com/2021/08/19/the-stretch-limo-of-game-boys/)，还有[一些在原始 Game Boy 外壳内填充现代计算平台](https://hackaday.com/2016/04/10/gameboy-case-lives-on-with-a-pi-zero/)。将 Game Boy 与 Hackintosh 结合起来绝对是一个新的发展，尽管这与[Ike]不同寻常的 Hackintosh 设计的历史非常吻合。

 [https://www.youtube.com/embed/Zust1wxkRt4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Zust1wxkRt4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

