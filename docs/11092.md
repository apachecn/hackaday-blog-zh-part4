# 用这个面部跟踪风扇保持凉爽

> 原文：<https://hackaday.com/2021/08/21/keep-cool-with-this-face-following-fan/>

[AchillesVM]决定[制造一个桌面电风扇](https://github.com/achillesvm/face_following_fan)，这样当他在房间里走动时，它就会跟踪他。平移和倾斜控制由一对由 Raspberry Pi 3b+控制的伺服系统提供。它怎么知道[achilles VM]在哪里？它使用 Raspberry Pi v2 相机捕捉场景，并使用 OpenCV 的默认面部跟踪算法来找到他。严格来说，它能追踪房间里任何人的脸。如果检测到多张脸，它会跟踪最大的一张，通常是最靠近粉丝的人。

整个处理循环以 60 毫秒运行，因此当涉及到跟踪快速移动的客人时，伺服机制的速度可能是限制因素。乍一看，它可能像是 20 世纪 20 年代的一个老粉丝，事实上[AchillesVM]自己建造了整个东西，3D 打印的外壳和使用一些现成的零件(如 25 厘米的遥控飞机螺旋桨)。

这是一项正在进行的工作，所以请关注他的 GitHub 库(如上)以获取更新。希望很快会有前置护手。如果你喜欢在你走动时与你互动的小工具，我们已经在 2014 年报道了[面部跟踪糖果大炮](https://hackaday.com/2014/01/13/the-face-tracking-confectionery-cannon/)，去年报道了[头部跟踪喷水枪](https://hackaday.com/2020/08/13/head-tracking-nes-water-blaster-is-good-summer-fun/)。在“不要尝试这个”的文件中，提到了开创事业的建筑——[眼球追踪激光机器人](https://hackaday.com/2017/04/18/robot-targets-eyeballs-fires-lasers-oshas-gonna-love-this-one/)。