# 设置菜单使用文本编辑器 Hack

> 原文：<https://hackaday.com/2022/01/20/setup-menu-uses-text-editor-hack/>

许多需要设置菜单的嵌入式设备将使用 USB 串行端口，您可以将该端口连接到您喜爱的终端仿真器。但我们最近遇到了一个通用 USB 旋钮，它使用文本编辑器进行设置，如记事本或 Vim(尽管这有点难看)。一家名为 iWit 的公司制造了几种 USB 旋钮，这些旋钮出现在许多这样的产品中。

这些通用 USB 旋钮通常是即插即用的，用于控制电脑的音量和静音。有些型号，如 iWit，用户可以[在设备](https://iwit.me/support/english.html)内配置映射。例如，旋钮旋转可以被设置为生成上下箭头键，且可以输入旋钮按压。人们可以在电脑上做这种映射，但许多 USB 旋钮可以为你做。设置的关键是这个菜单(你可以在下面视频的前 30 秒看到它的运行)。

```
- WINDOWS MODE -
1 Clockwise : Up Key
2 Counterclockwise : Down Key
3 Press : Enter
4 Press+Clockwise : Next
5 Press+Counterclockwise : Previous
6 Long Press : Play/Pause
[RESTORE DEFAULT]
[SAVE & QUIT]
```

这当然很好，但令人惊讶的是设置菜单是如何首先实现的。这个旋钮已经是一个 HID 了，它会弹出设置菜单，就像从键盘上输入一样。旋转旋钮选择一个选项会为上下移动光标生成 ANSI 转义序列，并以某种方式突出显示当前行。查看该流，您可以看到菜单是用这些代码处理的:

```
ESC [ 4 ~        Private code?
ESC [ 1 ; 2 H    Cursor row 1, col 2 
ESC [ D          Cursor back one column
ESC [ 3 ~        Private code?
```

而项目选择只是上下移动光标的代码:

```
ESC [ A          Cursor up one row
ESC [ B          Cursor down one row
```

如果我们在和一个终端对话，这是有意义的。但是还不完全清楚典型的文本编辑器如何处理 ANSI 转义序列。不难想象上下光标代码会被操作系统或编辑器本身解释为箭头键，但是突出显示仍然有点神秘。如果你有任何想法，或者你自己做过类似的事情，请在下面的评论中告诉我们。

下面的视频是在[Nelson Chu]的博客上找到的，他是一位专门在计算机图形系统中模拟有机笔触的艺术家。本文中使用的特定旋钮被标记为 DROK，因此您可能在您的 USB 旋钮中有此功能，即使它的标签上没有说 iWit。如果你想完全控制你的 USB 旋钮，就像我们在 2020 年的[这篇文章中所写的那样，打造你自己的 USB 旋钮。](https://hackaday.com/2020/07/06/multi-volume-knob-gives-all-your-programs-a-turn/)

 [https://www.youtube.com/embed/eR3obDyGL48?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/eR3obDyGL48?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

