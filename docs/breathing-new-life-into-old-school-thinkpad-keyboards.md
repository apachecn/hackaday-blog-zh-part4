# 给老式的 ThinkPad 键盘注入新的活力

> 原文：<https://hackaday.com/2020/05/26/breathing-new-life-into-old-school-thinkpad-keyboards/>

ThinkPad 通常被认为是黑客的非官方笔记本电脑，所以毫不奇怪，我们看到许多项目专注于修复和修改这些可靠的工作。但是，虽然我们通常看到人们在研究这种标志性计算机系列的相对现代的化身，但由[弗兰克·亚当斯]和[布莱恩·陈]进行的这个项目表明，[黑客对 ThinkPad 的热爱可以追溯到比许多人可能意识到的更远的地方。](https://hackaday.io/project/171439-ibm-thinkpad-380ed-keyboardtrackpoint-to-usb)

正如该项目的 Hackaday.io 页面上所解释的那样，两人制作了一个开放式硬件板，允许你从 90 年代末的 ThinkPad 380ED 上取下键盘和 trackpoint，并将其用作现代计算机上的标准 USB 输入设备。根据[Frank]的说法，这些电脑的键盘以全尺寸键而闻名，而不是今天如此普遍的“chicklet”板。

现在你可能想知道为什么这很重要。毕竟，我们已经看到很多项目将一个旧键盘连接到一个配有 USB 接口的微控制器上，让它们说通用语。这里的诀窍是，这些旧 ThinkPads 上的 trackpoint 实际上需要主板上的额外电路才能工作。键盘具有三个独立的 FPC 连接，分别用于矩阵、跟踪点按钮和跟踪点本身的模拟应变仪。

[![](img/ce0fe394fca420a595ea3498bdbb80f7.png)](https://hackaday.com/wp-content/uploads/2020/05/thinkpad380_detail.png)

经过大量的逆向工程，[Frank]和[Brian]开发出了一种板，它使用 Teensy 3.2 将过多的引脚变成有用的东西。在休息后的视频中，你可以看到新的复合 USB 设备在现代 Windows 计算机上完美地工作。

发现[弗兰克]对破解 ThinkPad 键盘并不陌生，这可能并不令人惊讶。在 2018 年，我们报道了他为更现代的 T61 打造的类似适配器，相比之下，这绝对是小菜一碟。

 [https://www.youtube.com/embed/WGSg1ky4UUs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WGSg1ky4UUs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

