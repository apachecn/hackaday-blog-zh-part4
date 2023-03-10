# 用鱼缸产生随机数

> 原文：<https://hackaday.com/2019/12/09/generating-random-numbers-with-a-fish-tank/>

在伦敦大学攻读计算和信息系统学位期间，[Jason Fenech]提交了一个有趣的提案，使用一个水族馆和一台足够高分辨率的摄像机来生成随机数。他的[鼓泡器不仅在操作](https://github.com/fenjas/bubblesrng)时发出相当放松的声音，而且根据 ENT、NIST-STS 和 DieHard 等工具的说法，它似乎是真正随机性的来源。

如果你想制作自己的泡泡器，你只需要一箱水和一些气泵来产生泡泡。一个俯视水面的网络摄像头捕捉到了当每个水泵产生的气泡柱碰撞时随之而来的混乱。在广告之后的视频中,[杰森]使用了两个水泵，但是考虑到[比](https://hackaday.com/2018/01/04/the-grooviest-random-number-generator-ever/)的熔岩灯便宜，我们可能会多扔几个进去。为了安全起见，他提到泵的位置和数量应该是任意的，并且在随后的安装中不能重复。

为了将这个微小的漩涡变成随机数的来源，OpenCV 首先用于识别视频流中位于用户提供的最小和最大半径之间的气泡。然后，软件捕捉每个气泡的 X 和 Y 坐标，得到的值被混洗和异或运算，直到一串随机数从另一端出来。当然，你如何利用这个无限不可能的廉价来源，取决于你自己。

虽然这个项目已经在互联网上流传了几年(没有双关语的意思),但它似乎在很大程度上被忽视了，只是由于我们一位杰出读者的提示才引起了我们的注意。这是一个很好的提醒，如果你在外面看到一些有趣的东西，[我们很乐意听到它的消息](https://hackaday.com/submit-a-tip/)。

 [https://www.youtube.com/embed/LUKy0Gaxn1g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LUKy0Gaxn1g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢大卫的提示。]