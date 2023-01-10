# 微控制器上的简化人工智能

> 原文：<https://hackaday.com/2019/11/29/simplified-ai-on-microcontrollers/>

人工智能正在席卷全球。然而，它似乎更像是让计算机自己解决问题的有用工具，而不是终结者式的启示录。这也不只是针对超级计算机。你也可以将人工智能加载到一些最小的微控制器上。Tensorflow Lite 是一个很受欢迎的工具，但让它在您特定的微控制器上工作可能会很痛苦，[除非您使用的是 Espruino](https://github.com/espruino/Espruino/tree/master/libs/tensorflow#actually-using-it) 。

这个项目为这类微控制器增加了对 Tensorflow 的支持，而不必使用笨拙的构建工具。基本上，添加一行代码就可以创建一个实例，而不需要编译任何东西，甚至不需要重启。Tensorflow 是一款用于微控制器的强大软件工具，现在可以使用它是一个巨大的飞跃。

那么，你能用这个工具做什么呢？这个项目背后的团队正在一款开放式智能手表上使用 Tensorflow，这款手表可以用来检测手势和许多其他事情。他们还开放了[这些工具用于浏览器](https://www.espruino.com/ide/emulator.html?gist=c0404a867b3531527428a1843c5fd5fc&upload)，允许使用人工智能软件并在不需要物理设备的情况下模拟 Espruino。这个有很多功能，而且它是开源的，可以变成你可能需要的任何东西，[就像把自己变成街头战士](https://hackaday.com/2019/09/18/arduino-accelerometer-and-tensorflow-make-you-a-real-world-street-fighter/)。