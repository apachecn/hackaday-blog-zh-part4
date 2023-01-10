# ESP8266 通过开源引擎开始游戏

> 原文：<https://hackaday.com/2019/03/11/esp8266-gets-its-game-on-with-open-source-engine/>

这可能不会让你感到震惊，但 ESP8266 非常受欢迎。在这一点上，我们更惊讶的是，当一个项目达到了提示线*而没有*利用这种极其便宜的支持 WiFi 的微控制器。如果你正在制作一个需要连接到互联网的小工具，那么 ESP 家族的某个成员很有可能是一个不错的选择。但是是一招 MCU 吗？

[![](img/6e4f9ce3b8a985967bb07ef1901e3d7d.png)](https://hackaday.com/wp-content/uploads/2019/03/espgame_detail-2.png)

ESP Little Game Engine Logo

嗯，从[软件框架来看，比如【Igor】](https://hackaday.io/project/164205-esp-little-game-engine)创建的“小游戏引擎”，看起来 ESP 也在将其触角伸向线下项目。虽然它可能不会将 ESP8266 变成下一代游戏强国，但我们不得不承认，迄今为止展示的演示令人印象深刻。当与几个按钮和一个 TFT 显示器(如 ILI9341)配对时，ESP 可以成为一个特别适合口袋的游戏系统。

[Igor]开发的游戏引擎为程序员提供了一个 128×128 的虚拟屏幕分辨率、一个背景层和 32 个精灵，这些精灵提供了碰撞检测和旋转等内置技巧。同时以每秒 20 帧的速度运行。这种环境对于主导 8 位和 16 位游戏时代的 2D 滚动游戏来说是理想的，正如在休息后的视频中看到的那样，它甚至可以完成一个相当不错的克隆*“Flappy Bird”。*

此外，[Igor]创造了一个在线仿真器和编译器，它允许你在你的网络浏览器中使用他的引擎开发游戏。你可以加载一些示例程序并执行它们来看看引擎的能力，然后在组装硬件之前尝试开发你自己的游戏。顺便提一下，这个在线开发环境的性能非常好；即使是相当复杂的“Flappy Bird”示例代码也几乎可以在模拟器中瞬间编译和启动。

这不是我们看到的第一款由 ESP8266 驱动的手持游戏，但可以公平地说，这款游戏是对其前辈的一次跨越。当然，如果你真的想开始扔一些像素，你可能会想作出的飞跃，以 ESP32 这是令人难以置信的令人敬畏的(和微小的)袖珍精灵的[心脏。](https://hackaday.com/2018/02/12/hands-on-with-the-smallest-game-boy-ever-made/)

 [https://www.youtube.com/embed/roOQHuXNVoI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/roOQHuXNVoI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/hUVykJf2aws?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hUVykJf2aws?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

