# DIY Arduino Due TEA5767 调频收音机

> 原文：<https://hackaday.com/2022/10/08/diy-arduino-due-tea5767-fm-radio/>

老黑客们会记得，水晶收音机通常是最先尝试的项目之一。时代变了，但是从空中收集看不见的信号，用自制的接收器听收音机，仍然有一些神奇的东西。[mircemk]已经将这个想法带到了最新的时代，建造了一个带有有机发光二极管显示器的调频收音机，由旋转编码器控制。

该设计相当简单，因为它是基于[mircemk]在另一个网站上找到的另一个项目，但构建看起来非常光滑，在任何黑客的工作台上都会占据首要位置。Arduino Due 构成了该项目的核心，控制 TEA5767 模块、SH1106 128×64 像素有机发光二极管显示器和旋转编码器。声音信号通过用于私人聆听的 LM4811 耳机放大器和用于内置扬声器的 PAM8403 类音频放大器传递。外壳由聚氯乙烯面板制成，并以彩色胶带突出风格。

通过连接预先构建的模块和从互联网上下载代码，像这样快速组合项目比以往任何时候都更容易，但这并不意味着这不是一种值得提高技能和制作一些像这样有用的设备的方法。如今有如此多的资源可供我们利用，站在巨人的肩膀上总是看得更远的好方法。

我们过去展示过一些使用 Arduinos 和 TEA5767 IC 的其他无线电项目，例如[这个在整洁的定制 PCB 上](https://hackaday.com/2020/12/04/fm-radio-from-scratch-using-an-arduino/)，以及[这个内置在旧无线电外壳中](https://hackaday.com/2015/07/02/retro-fit-old-radio-with-arduino-and-fm-module/)。

 [https://www.youtube.com/embed/idzZWg3VyX0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/idzZWg3VyX0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

