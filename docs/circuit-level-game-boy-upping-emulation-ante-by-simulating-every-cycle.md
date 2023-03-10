# 电路级游戏男孩:通过模拟每个周期来增加仿真赌注

> 原文：<https://hackaday.com/2019/04/23/circuit-level-game-boy-upping-emulation-ante-by-simulating-every-cycle/>

通常，在为像 Game Boy 这样的系统编写仿真软件时，为了减少仿真所需的资源，人们会尽可能地走捷径。然而，这具有令人遗憾的副作用，即它降低了仿真的整体准确性，并且降低了与系统上的游戏的兼容性。

这是项目背后的基本推理，这些项目寻求放弃简单化的抽象，支持周期精确、完全兼容的方法，其中 [MetroBoy](https://github.com/aappleby/MetroBoy) 可能是最极端的一个。它不是抽象掉硬件，而是在电路级进行仿真。和其他类似的项目一样，这意味着模拟器需要更多的 CPU 周期才能正常工作。从好的方面来看，人们仍然可以在任何现代系统上运行这个模拟器。

正如《都市男孩》作者[解释](https://www.reddit.com/r/EmuDev/comments/bfta48/metroboy_a_playable_circuitlevel_simulation_of_an/)的那样，他用 C++实现了代码，这使他能够以 [HDL](https://en.wikipedia.org/wiki/Hardware_description_language) 风格的方式构建电路，这在理论上也允许他在项目之外生成一个 Verilog(或 VHDL)软核。作为在 C++中实现 HDL 的一个演示，这无疑是很有趣的。

像这样的方法几乎与类似于 [UltraHLE](https://en.wikipedia.org/wiki/UltraHLE) (超高级仿真器)Nintendo 64 emulator 的项目完全相反，Nintendo 64 emulator 使用 Nintendo 64 游戏用 C 编写的知识作为创建库的第一步，Nintendo 64 ROMs 中的代码将调用这些库而不是本机(Nintendo)库。这使得 N64 游戏可以直接在目标系统上运行，UltraHLE 将图形和系统调用转换为本地操作系统调用，使用 3dfx Glide API 加速图形。

虽然像 UltraHLE took 这样的方法基本上完全放弃了仿真，从而最大限度地减少了系统资源的使用，但对于 Game Boy 这样的复古系统，游戏是在裸硬件上组装实现的，使用这种电路级仿真可以确保获得与原始手持控制台体验最精确的匹配。

对于那些现在渴望尝试 MetroBoy 的人来说，提醒一句，其 Github 网站指出，它目前缺乏对游戏保存的支持，使用原始 Game Boy (DMG)和 Game Boy Advance SP (AGS)硬件的混合，使一些游戏混淆，并且声音支持相当糟糕。

如果玩软件定义的游戏机电路还不够，还想看看真正的游戏机内部，那么文章顶部的 x 光图像是 Elektronaut 的 Chris 几年前完成的。