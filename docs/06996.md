# 人造老式收音机获得 AirPlay 升级

> 原文：<https://hackaday.com/2020/06/28/faux-vintage-radio-gets-airplay-upgrade/>

如今有很多复古风格的硬件，质量和功能混合在一起。[欢]发现了这样一个装置，它的外形是一个吸引人的蓝牙扬声器。决定他可以在保持原貌的同时改进功能，他开始着手黑客工作。

该项目的目的是保持原来的音量旋钮，按钮和屏幕，同时用一些更有能力的东西取代内部。树莓 Pi Zero 被用作操作的大脑，在早期尝试使用分立放大器面临嗡嗡声问题后，谷歌语音 AIY 硬件被用作声音输出。Arduino Pro Micro 被投入使用，以读取音量编码器和按钮，并驱动 charlieplexed LED 屏幕。然后在 Pi Zero 上安装了 Shairport Sync 来启用 Airplay 功能。

这是一个基本的黑客技术，但它给了[欢]一个有吸引力的 AirPlay 扬声器，以及大量使用 Arduinos 和 Raspberry Pis 的有用经验。我们以前也见过类似的黑客攻击。如果你正在家里制作你自己的立体声复活，[一定要给我们写信！](http://hackaday.com/submit-a-tip)