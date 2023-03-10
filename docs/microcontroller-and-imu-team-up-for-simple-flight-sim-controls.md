# 微控制器和 IMU 合作实现简单的飞行模拟控制

> 原文：<https://hackaday.com/2018/12/23/microcontroller-and-imu-team-up-for-simple-flight-sim-controls/>

康奈尔大学的课程已经结束，这意味着一件事:学习[布鲁斯·兰德]的微控制器设计课程的学生已经提交了他们的最终项目，其中许多项目，如谷歌地球飞行模拟器的飞行控制系统[，都找到了他们的 Hackaday tips 热线。](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2018/sb2276/sb2276/sb2276/index.html)

我们实际上在几天前得到了这个提示，但是因为它向我们揭示了以前未知的事实，即谷歌地球有一个飞行模拟器模式，我们有点分心。通常由鼠标和键盘控制，[希拉·巴鲁]决定给 sim 一整套飞行控制以使它更逼真。控制器由一个带油门的操纵杆、方向舵脚蹬和一个带随机开关的小型控制面板组成。整个系统都是用纸板建造的，以降低成本，并使系统易于复制。有趣的是，操纵杆没有通常安装在万向节上的电位计来检测俯仰和滚动；相反，安装在操纵杆顶部的 IMU 提供操纵杆位置的数据。所有控件都与 PIC32 对话，pic 32 通过串行电缆将输入发送到运行谷歌地球的 PC 上的 Python 脚本；该脚本模拟了驾驶 sim 卡所需的鼠标和键盘命令。下面的视频显示[希拉]驾驶一架 F-16 出去兜风，尽管她自己从 16 岁起就是一名飞行员，但奇怪的是，她无法将战斗机安全降落在郊区附近。

[布鲁斯]的课程看起来很棒，[希拉]显然很喜欢。我们期待着这个项目，它去年包括了[这个比利-山羊平衡 Stewart 平台](https://hackaday.com/2017/12/27/balance-like-a-mountain-goat-on-this-simple-stewart-platform/)和[一个机器人冰淇淋浇头器](https://hackaday.com/2017/12/26/an-automated-ice-cream-topper-for-the-ultimate-in-zero-effort-desserts/)。

 [https://www.youtube.com/embed/DWAt07CGMjs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DWAt07CGMjs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

