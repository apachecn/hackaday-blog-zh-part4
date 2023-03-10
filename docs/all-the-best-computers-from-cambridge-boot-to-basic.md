# 从剑桥 Boot 到 Basic，所有最好的电脑

> 原文：<https://hackaday.com/2021/02/01/all-the-best-computers-from-cambridge-boot-to-basic/>

Raspberry Pi 是一个出现在许多逆向计算项目中的优秀机器，但是它的定制 Linux 发行版缺少一样东西。它引导到 GNU/Linux shell 或全功能桌面 GUI，而不是像正常计算机那样引导到基本解释器。这让怀念早期 ROM BASIC 的艾伦·波普(Alan Pope)很恼火，所以他着手创建一个树莓 Pi 400，让用户直接使用 BASIC。接下来的内容远远超出了 Pi 的范围，因为他从“基本状态”的角度审视了这种简单编码语言的各种可用解释器。几乎你能想到的每一种主流口味都有一个解释器，但作为一台运行 ARM 处理器的剑桥电脑的合适选择，他选择了一个提供 BBC BASIC 的解释器。

当然可以编写一个裸机映像，让用户直接使用原生的 ARM BASIC 解释器，但是他选择了在极简的 Linux 映像上运行解释器的更安全的途径。在这里，他采取了意想不到的步骤，使用 Ubuntu 发行版而不是 Raspberry Pi 操作系统，这是通过熟悉它的怪癖完成的。最终，他选定了一个 BBC BASIC 解释器，该解释器允许他通过 SDL 库完成所有的图形技巧，而不需要 X 或合成器的提示，这意味着他终于有了一个引导到 BASIC 的 Pi。假设它是一个解释器而不是仿真器，它应该比原来的要快得多，但他没有与我们分享这些信息。

这个[不是我们给你展示的第一个引导至基本机器](https://hackaday.com/2020/06/23/boot-to-basic-box-packs-a-killer-graphics-engine/)。

标题图片:一个真实的 BBC Micro BASIC 提示。感谢[克莱尔奥斯本]的图片。