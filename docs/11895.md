# 万圣节游戏让你用激光驱动的十字弓射击僵尸

> 原文：<https://hackaday.com/2021/11/12/halloween-game-lets-you-shoot-zombies-with-a-laser-powered-crossbow/>

假设你正在寻找制作一个伟大的万圣节主题射击游戏的所有必要元素。僵尸？检查。巨型“激光器”？检查。弩射叉？我们会掩护你的。看看“[叉僵尸](https://www.instructables.com/Fork-the-Zombies-an-Interactive-Halloween-Game/)”，这是由[pills . of . spam]在今年万圣节为娱乐邻居的孩子而设立的。

游戏在大屏幕上进行，屏幕上显示一群愤怒的僵尸向玩家行进，玩家必须在他们到达屏幕前尽可能多地射击。提供的武器是弩；当扳机被扣动时，一把叉子被发射出去，希望能叉住其中一个食尸鬼。这款游戏是使用名为 [Urho3D](https://urho3d.io/) 的开源引擎编写的，该引擎负责所有核心的 3D 和物理工作，允许用户专注于设计游戏和视觉效果。

为了让游戏更具物理感，[成堆的垃圾邮件]制作了一个真正的弩供玩家使用。它的手柄是从一块废木头上切割下来的，使用带锯切割出大致的形状，使用 CNC 机器切割出精致的切口，这些切口包含一个激光指示器、一个 ESP32 和一个基于微动开关的触发器。当扣动扳机时，激光照射到游戏屏幕上，而 ESP32 通过 WiFi 发送数据包。

使用一个聪明的技巧来跟踪拍摄的位置:一个网络摄像头对准屏幕，前面有一个红色的滤色镜。这样，它只能看到红色激光点在屏幕上移动。使用 Python OpenCV 库处理生成的图像，该库提供了将指针在屏幕上的相对运动转换为沿运动场的绝对位置的函数。

计算硬件由一对 Jetson Nano 板组成，它配备了四核 ARM A57 CPUs 以及强大的图形硬件来生成游戏的视觉效果。最终结果令人印象深刻，特别是考虑到所有这些都是在短短三周内设计和建造的。这显然是一个巨大的成功，因为游客排队试图拍摄饥饿的僵尸。

激光笔是创建射击游戏的一个明显的工具:我们已经看到过有[单个圆形目标](https://hackaday.com/2020/05/08/open-laser-blaster-shells-out-more-bang-for-the-buck/)，一组[形状设置在你周围](https://hackaday.com/2020/01/14/node-red-laser-shooting-gallery-goes-anywhere/)，甚至还有[金属罐倒下并重新站起来](https://hackaday.com/2012/01/03/laser-shooting-gallery-made-from-scrap/)。但是如果你需要在真正的僵尸末日来临时保护自己，一个发射刀子的[弹弓可能会更有用。](https://hackaday.com/2011/03/30/stupid-expert-builds-a-machete-slingshot-for-the-impending-zombie-apocalypse/)

 [https://www.youtube.com/embed/ALwMA8c7ayg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ALwMA8c7ayg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

