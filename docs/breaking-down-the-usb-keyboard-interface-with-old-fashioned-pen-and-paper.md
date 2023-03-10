# 用老式纸笔分解 USB 键盘接口

> 原文：<https://hackaday.com/2021/06/24/breaking-down-the-usb-keyboard-interface-with-old-fashioned-pen-and-paper/>

老式 PS/2 风格键盘和现代 USB 设备哪个更适合玩游戏？[Ben Eater]开始回答这个问题，但是在这个过程中，他最终破坏了整个 USB 键盘接口。

原来 PS/2 和 USB 是非常非常不一样的。只要有电，PS/2 键盘会在您每次按键时发送您的击键。USB 键盘更有礼貌，它不会把你的击键发送到电脑，直到电脑要求它们。

为了帮助我们理解 USB 更复杂的事务，[Ben]打印出了 PC 和键盘之间 USB 交换的示波器轨迹，并使用一支笔和 USB 规范对其进行了解密。我们惊讶地发现，USB D+和 D-线不仅仅是一个差分对，还具有更复杂的信号行为。为了研究 USB 如何处理多键翻转，[Ben]甚至借来了一个奇特的示波器，可以自动解码 USB 数据包。

事实证明，新的并不总是更好——测试的廉价低速 USB 键盘[Ben]比他值得信赖的 PS/2 型号慢得多，即使是使用更快的全速 USB 协议的更好的键盘也只是和 PS/2 一样快。

如果你想更深入地研究键盘协议，请查看[【Ben】的 PS/2 键盘接口指南](https://hackaday.com/2021/03/11/decoding-the-ps-2-keyboard-protocol-using-good-old-fashioned-hardware/)，包括一个试验板硬件解码器。如果这些键盘的按键太多，你可能会考虑这个 [USB 莫尔斯电码键盘](https://hackaday.com/2017/01/25/tiny-morse-code-usb-keyboard/)。感谢彼得·马丁的提示！