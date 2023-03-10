# Scramblepad 拆卸揭示复杂，昂贵的内部结构

> 原文：<https://hackaday.com/2022/11/18/scramblepad-teardown-reveals-complicated-expensive-innards/>

什么是 Scramblepad？这是一种数字键盘，其中的数字不在固定的位置，只能从狭窄的视角看到。每次激活键盘时，按钮都有不同的数字。这样一来，一个固定的数字代码就不会被按键磨损或手指敲击时的位置显示出来。[Glen Akins]去年得到了一个，并想出了如何与它连接，[分享了大量漂亮的照片和细节](https://bikerglen.com/blog/the-scramblepad-hardware-and-protocol/)关于这个设备内部有多复杂。

[![](img/072f473be2561d2e4f4cd95dda874ce0.png)](https://hackaday.com/wp-content/uploads/2022/11/05.led-display-board.jpg)

Just one of the many layers inside the Scramblepad.

1982 年获得专利，用于访问控制，一个扰频板旨在避免有人通过观察用户输入密码来推断密码的风险，同时也防止通过按键本身的磨损而泄露信息。它们被设计用来解决一些特定的问题，但是正如[Glen]指出的，有很多很好的理由它们今天没有被使用。不仅它们的可访问性差(它们只能在特定的高度和视角下工作，视力受损的人无法访问)，而且最重要的是它们复杂、昂贵，并且不防破坏。

[Glen]的 Scramblepad 可能已经过时，但凭借其黑色的构造、锐利的线条和红色 LED 7 段显示屏，它拥有不可否认的风格。它还包括一个 RFID 阅读器，允许它作为一种双因素访问控制。

在内部，阅读器是一个巨大的硬件，有多层印刷电路板和天线。尽管所有的电子设备都塞进了 Scramblepad，但它本身并没有做多少事情。中央控制器实际上控制门的进入，pad 通过未加密的专有协议与该板通信。[Glen]完成了解码工作，并设计了一个简化的板，他计划用于自己的门禁控制器。

与此同时，这是一个很好的窥视一个整洁的硬件。你可以在下面的视频短片中看到[Glen]的 Scramblepad。

 [https://www.youtube.com/embed/aKK6tlvxios?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aKK6tlvxios?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

