# Arduino 手持游戏系统获得了抓地力

> 原文：<https://hackaday.com/2020/02/06/arduino-handheld-game-system-gets-a-grip/>

只需一个 Arduino、一个有机发光二极管显示器和一些按钮，就可以轻松构建自己的仿复古游戏系统。甚至有越来越多的针对这种特定硬件组合的图书，这在很大程度上要归功于 Arduboy 项目。但是，除非你满足于在试验板上玩 *Circuit Dude* ，否则在某些时候，你可能会想用一种更方便的形式来包装构建。

像之前的许多产品一样，由 Alex Zidros 创造的有机发光二极管掌机从任天堂的一个产品中获得灵感；但不是游戏机。相反，[他的设计是基于他在 Thingiverse 上找到的开关 Joy-Cons](https://github.com/aziddy/Mini-OLED-Retro-Handheld) 的 3D 打印手柄。在安装了印刷电路板的支架后，他拥有了一个相当独特的系统。

[![](img/c33f04dbb1597533fafbaeba86f212cc.png)](https://hackaday.com/wp-content/uploads/2020/02/ardugrip_detail.jpg) 我们特别喜欢偏置 SSD1306 有机发光二极管显示器。不是因为我们认为一个不对称布局的游戏系统是一个特别合理的设计决策，而是因为它给了整个游戏一种赛博朋克的感觉。当与暴露在外的电子设备结合在一起时，整个系统看起来就像是从一个未来垃圾箱中拼凑出来的。就我们而言，这是高度赞扬。

显示器的对面是一个脂肪袋电池，[Alex]说这是从便携式扬声器中解放出来的，下面是 Adafruit Feather 328P。有两个触觉开关安装在羽毛的前面，与这种构造不同的是，在 3D 打印外壳的肩部还有两个。所有的东西都是由一块 perfboard 碎片组成的，这使得任何想要构建自己版本的人都很容易。

如果你喜欢你的 Arduino 和有机发光二极管游戏以稍微熟悉的形式出现，[在 Dreamcast 视觉记忆单元(VMU)](https://hackaday.com/2019/07/15/aruboy-in-a-dreamcast-vmu/) 内完成的构建一直是这些部件的最爱。