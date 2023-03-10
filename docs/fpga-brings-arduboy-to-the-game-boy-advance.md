# FPGA 为 Game Boy Advance 带来 Arduboy

> 原文：<https://hackaday.com/2019/02/21/fpga-brings-arduboy-to-the-game-boy-advance/>

Hackaday 的读者可能熟悉 Arduboy，这是一个开源手持游戏系统，旨在将 Arduino 开发的便捷性与互联网对最初的任天堂游戏男孩的强烈怀旧情绪结合起来。虽然与为“真实”系统发布一款游戏不太一样，但 Arduboy 平台的开源特性允许个人开发一款可在商业制造的设备上运行的游戏。

虽然 Arduboy 的硬件本身确实非常漂亮，但这并没有阻止人们试图将它的游戏带到其他硬件上。现在，由于[uXe]的努力，[Game Boy Advance 正在成为兼容 Arduboy 的](https://github.com/uXeBoy/GBArduboy)，在某种程度上使整个项目圆满完成。假设这个小工具变成了一个商业设备(听起来好像还悬而未决)，Arduboy 开发者将能够自豪地在最终和客观上最好的进入 Game Boy 系列的游戏中发挥他们的创造。

正如 Arduboy 论坛上的一个帖子所记录的那样，[走到这一步有点冒险。社区成员想知道如何才能让 Arduboy 游戏在真正的 Game Boy 上运行，但很快就发现最初的米色砖块模型并不能胜任这项任务。最终，其更有能力的继任者 Game Boy Advance 成为了开发目标，并考虑了不同的方法来让现有的游戏在该平台上运行。](https://community.arduboy.com/t/arduino-gameboy-cartridge/7057/2)

虽然有一些有趣的想法，例如使用 GBA 的链接端口通过 SPI“馈送”系统游戏，但最终[uXe]决定研究创建一个 FPGA 卡盒，实际运行 Arduboy 游戏。在这种情况下，GBA 本身基本上只是用作 FPGA 和人类玩家之间的接口。除了这些低级的硬件考虑之外，还有很多关于将游戏带到新硬件的更实际的方面的讨论，例如如何最好地将 Arduboy 的 128 x 64 输出扩展到 GBA 的 240 x 160 屏幕。

正如休息后的视频所展示的，[uXe]现在是在 GBA 上玩 Arduboy 游戏的所有元素，包括通过使用肩部按钮禁用全屏缩放的能力。现在，他只需要将硬件缩小到可以放入标准 GBA 墨盒的程度。除此之外，谁知道呢？也许能够在真正的游戏机上运行 Arduboy 游戏的吸引力足以保证将这种黑客技术变成一种新的商业产品。

由于硬件互换[，我们已经看到 Arduboy 游戏在 Dreamcast VMU](https://hackaday.com/2019/02/04/arduboy-brings-new-life-to-dreamcast-vmu/) 上运行，而【uXe】自己以前[将 Arduboy 兼容的硬件移植到原始 Game Boy](https://hackaday.com/2015/08/18/arduboy-classic-plays-on-original-game-boy-screen/) 上，但能够在未经修改的 Game Boy Advance 上运行这些游戏显然有其自身的吸引力。至少，它会比使用一个被黑掉的教室小工具更符合人体工程学一点[。](https://hackaday.com/2018/07/22/classroom-gadget-turned-arduino-compatible/)

 [https://www.youtube.com/embed/h-wpDa2p5C8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/h-wpDa2p5C8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/aJvbZW5do2w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aJvbZW5do2w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

