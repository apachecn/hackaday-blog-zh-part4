# 机器人旋律一个学生很热情，但很糟糕

> 原文：<https://hackaday.com/2020/12/31/robotic-melodica-student-is-enthusuastic-but-terrible/>

任何经历过第一次学习演奏一种乐器的过程的人，或者听到有人试图这样做的人都会知道，这可能是一种相当痛苦和令人沮丧的经历。显然，亚历山德罗·佩里尼(Alessandro Perini)无法从第一次接触音乐的人那里获得足够的声音，所以他创造了一个机器人来连续几个小时演奏糟糕的旋律，就像休息后的视频中展示的那样。

该项目被恰当地命名为“人工智能刚刚开始学习演奏”，并试图实时复制它听到的每一段旋律。这个机器人由一台旧打印机的墨盒托架组成，安装在一个木制框架上以支撑 melodica。最初的托架使用带有编码器的 DC 电机来实现精确移动，但是由于位置精度不理想，[Alessandro]放弃了编码器。两个小滚轮安装在墨盒支架上，用于按下 melodica 的按键。双稳态电磁阀控制从空气压缩机到 melodica 的气流。DC 电机和电磁阀由 Arduino 通过一对 LM298 电机驱动器控制。

运行用[Cycling’74 MAX](https://hackaday.com/2020/12/17/remoticon-video-how-to-use-max-in-your-interactive-projects/)编写的软件的主机会听到它试图模仿的旋律，并向 Arduino 发送串行命令，以移动托架并打开螺线管来尝试匹配音符。当然，它在这个过程中不断地打出一连串错误的音符。 [Arduino 代码和构建指令已经公布](https://www.hackster.io/touchmysound/self-playing-melodica-866128)，但是主要的 Max 软件只是简单描述一下。[Alessandro]在当地的一个节日上展示了这个机器人，在那里它播放了 YouTube 教程片段，并与当地的一个乐队一起演奏了整整 24 小时。你必须尊重这种忍耐力。

如果听不太容易出错的电子控制乐器更合你的口味，听听这个[建筑大小的管风琴演奏 MIDI 文件](https://hackaday.com/2020/04/09/controlling-a-building-sized-pipe-organ-with-midi/)。

 [https://www.youtube.com/embed/uYKpWY6NF2c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uYKpWY6NF2c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

