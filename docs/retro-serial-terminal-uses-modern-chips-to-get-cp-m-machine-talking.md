# 复古串行终端使用现代芯片让 CP/M 机说话

> 原文：<https://hackaday.com/2022/03/06/retro-serial-terminal-uses-modern-chips-to-get-cp-m-machine-talking/>

家用电脑时代早期的爱好者用当时相对原始的芯片创造了奇迹，Z80 或 6502 无法完成的事情通常被归入基于逻辑芯片和分立元件的复杂设计。人们不禁要问，这些黑客用我们认为理所当然的现代组件能完成什么。

也许它会是类似于[这种小型串行终端](https://hackaday.io/project/184235-60x25-minimal-terminal)的东西，用于当前的自制复古计算机。该电路板由[Augusto Baffa]制造，用于[的 Baffa-2 自制微型计算机](https://hackaday.io/project/183266-baffa-2-homebrew-microcomputer)，这是一台运行 CP/M 的 RC2014 型 Z80 机器。该端子板是插入 Baffa-2 背板的许多外围电路板之一，但它是少数几个似乎走捷径使用现代微控制器完成工作的电路板之一。板上有一对 ATmega328s 一个处理与 Baffa-2 背板的串行通信，另一个负责运行 VGA 接口。该卡还具有 PS/2 键盘接口，并支持 VT-100 ANSI 转义。下面的视频展示了它在 17 英寸液晶显示器上的运行，屏幕宽高比为 4:3。

我们喜欢这种终端卡简单方便地完成工作的方式，我们也非常喜欢 Baffa-2 本身的外观。我们还在视频背景中发现了一台 IMSAI 8080 和一台 Altair 8800。我们很想知道更多。

 [https://www.youtube.com/embed/mmQTUNvmSpk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mmQTUNvmSpk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

