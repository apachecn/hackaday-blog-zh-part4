# 游戏男孩在 Verilog 中重新创建

> 原文：<https://hackaday.com/2019/03/23/game-boy-recreated-in-verilog/>

随着 Raspberry Pi 硬件的广泛使用和带有模拟器的预烤 Linux 发行版的推出，制作复古手持设备比以往任何时候都更容易。然而，模仿并不是玩旧游戏的唯一方式。[张文婷]决定用 Verilog 重新制作任天堂游戏机，并记录了这一努力。

该项目在 Spartan 6 FPGA 上运行。[文婷]首先开发了使用双冲击控制器输入的硬件，并将视频输出到普通的液晶显示器。然而，生产手持 VerilogBoy 的工作正在进行中。这将采用 320×320 的 LCD 屏幕，像素是最初 Game Boy 160×144 分辨率的四倍，还有一些像素备用。[文婷]也在考虑将代码移植到一些 Pano 逻辑单元上，我们之前已经讨论过了。瘦客户机包含 FPGA 硬件和大量 IO 端口，非常适合此类项目。

Github 上为好奇的修补者提供了代码。虽然有更简单的方法来玩旧的掌上游戏，但这样一个项目的学习价值不应该被低估。我们已经看到 FPGAs 也用于其他任天堂 hi jinx——像这个 NES 推车，包装一些严重的肌肉。休息后的视频。

 [https://www.youtube.com/embed/wMJI7j6YY3A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wMJI7j6YY3A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/co_hXEwh5SI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/co_hXEwh5SI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

