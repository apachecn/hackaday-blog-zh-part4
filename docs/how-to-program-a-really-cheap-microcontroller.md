# 如何编程一个真正便宜的微控制器

> 原文：<https://hackaday.com/2019/02/17/how-to-program-a-really-cheap-microcontroller/>

有传言说有一种廉价的芯片，它本身支持 USB，有一个开源工具链，价格只有四分之一。这些不是谣言:你现在就可以买到 CH552 微控制器。令人惊讶的是，没有多少人会为他们的下一个项目选择这种廉价的芯片。如果没有原始项目使用这种芯片，没有人会使用这种芯片。第 22 条军规等等。

像一个慷慨的上帝一样， [[Aaron Christophel]为你提供了一个编程这个廉价芯片的工作示例](https://www.youtube.com/watch?v=IDCQNa2ywiM)，并用它做一些有用的事情。它能使发光二极管闪烁，能向 I2C 显示器写入数据，能做任何你想从一个只值几毛钱的微控制器上得到的东西。

CH552，以及它的朋友小 CH551 一直到 CH559，包含一个 8051 内核，大约 16 kB 的闪存，高端芯片有一个 USB 控制器，有 SPI，PWM，I2C，成本很低。不像其他芯片，你可以找到 SDK 和工具链。你可以通过 USB 给芯片编程。很明显，如果有人为它编写了 Arduino 包装器，我们会看到非常酷的东西。我们还没到那一步，但已经很接近了。

为了给这些芯片编程，[Aaron]首先必须将微控制器连接到电路中。这只是一点性能板，一个电阻，几个帽子，和一个 USB 插头。就这样，这就是所需要的。这是一个相当标准的 8051 内核，因此编写代码相对容易。上传是通过 [WCHISPTool 软件](http://www.wch.cn/download/WCHISPTool_Setup_exe.html)完成的，带有您喜欢的*nix 风格的选项。

但事情会变得更好。CH552 的一大特色就是 USB。这意味着没有昂贵或怪异的程序员，是的，但这也意味着 CH552 可以模拟 USB HID 设备。CH552 可以变成 USB 键盘。为了演示这一点，【Aaron】[编写了一个 CH552 板](http://atcnetz.blogspot.com/2019/02/ch552-020-mikrocontroller-mit-usb.html) (DE，这里是 [Google translatrix](https://translate.google.com/translate?sl=auto&tl=en&js=y&prev=_t&hl=en&ie=UTF-8&u=http://atcnetz.blogspot.com/2019/02/ch552-020-mikrocontroller-mit-usb.html#more&edit-text=&act=url) )装载了触摸板和 led，成为一个 USB 键盘。

如果你不想自己焊接其中一个，CH554 开发板的供应商有[家](https://www.electrodragon.com/product/ch552-ch554-mini-dev-board-ch55x-series/)，这里有【亚伦】的项目[的文件](http://atcnetz.blogspot.com/p/downloads.html)。查看下面的视频，因为这是关于编程和使用一些刚刚上市的非常有趣的芯片的最佳教程。

 [https://www.youtube.com/embed/IDCQNa2ywiM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IDCQNa2ywiM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/cSYMe4xyGeo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cSYMe4xyGeo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

