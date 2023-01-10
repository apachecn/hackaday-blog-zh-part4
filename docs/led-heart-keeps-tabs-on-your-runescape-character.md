# 发光二极管心脏保持标签在你的江湖人物

> 原文：<https://hackaday.com/2022/06/02/led-heart-keeps-tabs-on-your-runescape-character/>

MMORPG 江湖在 21 世纪初的玩家心中有着特殊的地位。当然，以现代的标准来看，这可能显得特别古怪，但在当时，这是开创性的东西。另外，你可以免费玩，这当然有助于人们参与进来。虽然有一个更现代的版本可用，但许多早期玩过这款游戏的人更喜欢坚持他们所知道的，并继续运行现在被称为*老派江湖*的游戏版本。

[Austin Blake]是早期采用者之一，他在这个 LED 健康指示器中投入的[工作应该告诉你所有你需要知道的关于他对经典游戏有多投入的信息。3D 打印的心脏拥有令人难以置信的 312 个新像素的 led，它们由背面的 5 伏兼容 Arduino Nano 控制。心脏的颜色和“填充水平”都会实时变化，以适应玩家角色的健康状况。](https://www.youtube.com/watch?v=TdxfkXpm_T4)

[![](img/d9a383d63eae07ecc36dbf6ae92eab8a.png)](https://hackaday.com/wp-content/uploads/2022/06/runeheart_detail.jpg) 建造光明本身相当简单，但从游戏中获得生命值却是另一回事。正如[奥斯汀]在视频中解释的那样，他的第一次尝试涉及使用 Python 和一些图像识别例程来从屏幕上读取指示器。这个想法很有效，坦率地说，它本身就是一个值得记住的迷人技巧，但不幸的是，它太慢了，无法提供他所寻求的实时反馈。

最终，他将注意力转向了 rune lite T1，这是一个为 T2 守旧派 rune scape T3 开发的开源客户端。由于它的开源性质，他可以编写一个例程来读取当前的健康值并将其发送到 Arduino，但由于一个成熟的插件系统，他不必这样做。

游戏的 API 让他创建了一种简单可靠的方法来从游戏中获取数据，类似于我们在飞行模拟器社区中看到的用于驱动物理仪表和显示器的。 *RuneLite* 拥有一个社区开发的插件库，并且【奥斯汀】说如果其他人对构建类似的指标感兴趣，他很乐意提交他的插件——这是[与这种运动感应 *RuneScape* axe](https://hackaday.com/2021/12/02/play-runescape-irl/) 的完美匹配。

 [https://www.youtube.com/embed/TdxfkXpm_T4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TdxfkXpm_T4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

