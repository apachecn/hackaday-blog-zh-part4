# 把你的车变成一个模拟器

> 原文：<https://hackaday.com/2019/05/14/turn-your-car-into-a-simulator/>

电子游戏固然有趣，但也是体验现实生活中不容易重现的事物的好方法。在太空中的巨型环上拍摄外星人是一个明显的例子，但还有一些更现实的例子，视频游戏使这些例子变得更容易理解，例如驾驶赛车。你也可以让这种体验变得尽可能真实，而且[甚至可以使用一辆真正的汽车作为你的控制器](https://github.com/aarossig/can-joystick)。

所有现代汽车都使用通信系统，使它们的各种模块能够相互交流。燃油喷射、油门位置、踏板位置、方向盘角度和气候控制系统都可以在 can 总线上通信，通过利用这些信息，汽车可以用作视频游戏的控制器。一旦你插入汽车的 OBD-II 端口，你将需要一个软件来解码所有的信息。[Andrew]使用 uinput，这是一个允许 Linux 机器获取任何输入信号并以任何可编程的方式映射它的工具。

该构建还包括集成微型投影仪的使用，允许汽车随时停放并变成模拟器。这类似于另一个使用马自达而不是雪佛兰 Volt 的项目，但它只是表明从现代汽车的 can 总线获取信息是多么简单。

 [https://www.youtube.com/embed/F_Phf7zzg-k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/F_Phf7zzg-k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

