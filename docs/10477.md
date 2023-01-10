# 在自制的 8 位计算机上从头开始使用 VGA

> 原文：<https://hackaday.com/2021/06/21/vga-from-scratch-on-a-homebrew-8-bit-computer/>

[詹姆斯·沙曼]制造了一台令人印象深刻的 8 位自制电脑。基于 TTL 逻辑芯片，它有一个流水线设计，这使它能够进行准将级的计算，但[詹姆斯]还没有完全完成一切。虽然它目前是建立在自己的定制 PCB 上，但它有一个有限的 LCD 显示屏，达不到其余部分的标准。为了解决这个问题，他决定从头开始实现 VGA。

这也不是一个简单的 VGA 实现。他计划采用全分辨率(640×480)，这将推动他的硬件极限。他还设定了 24 位 DAC 的目标，这将允许数百万种颜色、使用精灵的能力和硬件滚动。因为他是从零开始做这些的，所以他的计划是尽可能地保持简单，并且在他做的过程中逐步改进构建。为此，第一次迭代使用单个锁存芯片和一些其他无源元件。在给 CPU 添加一些代码以支持新的视频风格后，[James]能够在他的显示器上显示图像。

虽然他展示的鹦鹉形象还不完美，但这对他的构建来说是一个很好的开始，他确实计划在未来的视频中对它进行改进。我们可以说他正在复制一台完整的 8 位逆向计算机。尽管 VGA 对于现代计算机来说早已过时，但该标准易于实现，有限的版本[甚至可以在非常小的微控制器](https://hackaday.com/2015/12/17/attiny-does-170x240-vga-with-8-colors/)上实现。

感谢[BaldPower]的提示！

 [https://www.youtube.com/embed/K658R321f7I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/K658R321f7I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

