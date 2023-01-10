# 用机器人雨人让牌落在它们可能落的地方

> 原文：<https://hackaday.com/2019/06/13/let-the-cards-fall-where-they-may-with-a-robotic-rain-main/>

最后，机器视觉的一个有用的应用！忘记那些无人驾驶的废话和面部识别的东西吧——我们终于有了一个可以在 21 点桌上算牌的人工智能。

[Edje Electronics]建立的系统被称为“雨人 2.0”，以纪念[达斯汀·霍夫曼]为 1988 年电影中的[创造的经典角色，旨在通过算牌将 21 点桌上的赔率从赌场转移出去。他在下面的视频中解释了这样一种策略，高低计数，雨人 2.0 在网络摄像头和 YOLO 的帮助下实现了实时物体检测。由于[Edje]通过 OpenCV 的一些欺骗手段综合生成了大量的卡片图像训练集，因此可以根据卡片的花色和等级在任何方向检测卡片。一个脚本自动完成了这个过程，并为 YOLO 生成了一个由 5 万张图片组成的丰富的训练集。Python 程序将训练好的模型实现到实时纸牌计数应用程序中。](https://www.imdb.com/title/tt0095953/)

雨人 2.0 是对[【Edje】早期张量流卡计数器](https://hackaday.com/2018/05/23/using-tensorflow-to-recognize-your-own-objects/)的改进，但仍有局限性。它不能像虚构的[雨人]那样算作一双六层鞋，至少现在还不能。尽管如今骗子的正义可能不全是[的牛刺和锤子](https://www.youtube.com/watch?v=2Nf6S9miiHg)，但这种黑客行为所需的硬件也不太可能逃过赌场的安检。所以[Edje]明智地将其用途限制在练习算牌技巧上。最终，他想把雨人变成一个完全的人工智能 21 点玩家，并探索它在其他游戏中的潜力，并帮助视力障碍者。

 [https://www.youtube.com/embed/Nf3zBJ2cDAs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Nf3zBJ2cDAs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

