# 线路板计算机在字符显示器上玩蛇；还在一个浏览器里！

> 原文：<https://hackaday.com/2020/04/26/breadboard-computer-plays-snake-on-character-display-also-in-a-browser/>

如果你喜欢在试验板上制作自制电脑，你肯定很熟悉[Ben Eater]，他只用逻辑门的设计多年来一直是许多复制品的灵感来源。[【vis realm】采用了这个概念并加以扩展](https://cpu.visualrealmsoftware.com/)，甚至增加了一个 16×2 的 LCD，让[你可以通过移动角色显示器上的一个像素来玩蛇](https://www.youtube.com/watch?v=xVAOxb0N3pg)！

充分利用微小的分辨率令人印象深刻——这是游戏领域的一个困难制约。但是还有其他的技巧在起作用。[visrealm]使用不同的强度来区分蛇和它的食物，这在休息后显示的演示中是一种黑暗的像素。但最突出的是，试验板的构建实际上只是故事的一半。此外，[visrealm]构建了一个完整的模拟器，类似于他的实际试验板设计[，可以通过浏览器](https://cpu.visualrealmsoftware.com/asm/)进行编程和使用，赋予 WebAssembly 一个全新的含义。虽然这对任何有兴趣玩这些试验板计算机，但缺乏耐心自己建造一台的人来说都很方便，但它也可以作为真正的编程环境。此外，ESP8266 用于通过 WiFi 直接加载新程序。

所有代码和一些构建说明都可以在 GitHub 上找到[，如果你正在为你的网站寻找一个漂亮的 LCD 模拟器，](https://github.com/visrealm/vrcpu)[也有一个独立的资源库](https://github.com/visrealm/vrEmuLcd)。但是如果你需要一个更好的显示选项给你自己的试验板电脑，[增加一个 VGA 连接器](https://hackaday.com/2019/07/17/pushing-pixels-to-a-display-with-vga-without-a-pc/)怎么样？如果你还没有建立你自己的系统，那么[开始](https://hackaday.com/2017/04/10/8-bit-breadboard-computer-is-up-to-8-hours/)永远都不晚。

 [https://www.youtube.com/embed/xVAOxb0N3pg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xVAOxb0N3pg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

