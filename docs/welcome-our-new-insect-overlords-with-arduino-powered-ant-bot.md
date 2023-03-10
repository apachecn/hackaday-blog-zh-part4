# 用 Arduino 驱动的蚂蚁机器人欢迎我们的新昆虫霸主

> 原文：<https://hackaday.com/2018/12/17/welcome-our-new-insect-overlords-with-arduino-powered-ant-bot/>

步行机器人有多种形式，每一种都有自己独特的挑战。双足式运动被认为是特别难做好的，然而有更多腿的设计提供了某些优势。六足动物提供了在其他腿移动时保持几条腿在地面上的可能性，提供了有用的稳定性。[【How To Mechatronics】开发了这个蚂蚁机器人](https://howtomechatronics.com/projects/arduino-ant-hexapod-robot/)，就是形态的绝佳例子。

顾名思义，六足动物有六条腿，每条腿由三个关节组成。这需要每条腿 3 个伺服系统，总共 18 个伺服系统只是为了移动。然后进一步使用伺服系统来控制腹部、头部和下颌骨。这给了机器人强大的蚂蚁凭证，不仅仅是简单的 3D 打印外观。

大脑来自 Arduino Mega，因其控制大量伺服系统的能力而被选中。印刷定制的 PCB 作为屏蔽，以方便所有必要硬件的连接。HC-05 蓝牙模块用于与控制 ant 的 Android 应用程序进行通信。抵抗的一部分是头部的超声波传感器，它允许蚂蚁自动保护自己免受太近的捕食者的攻击。

这是一个复杂的建筑，需要大量的 3D 打印和 200 多个紧固件。尽管从根本上来说，它是一个完全工作和测试过的六足建筑，有完整的计划可供下载，[准备好在你的地下糖洞穴中辛苦工作](https://youtu.be/W4jWAwUb63c?t=40)。

如果你的六足动物更偏向于动漫而不是昆虫类，那么[看看这个外壳中的幽灵](https://hackaday.com/2016/06/03/hexapod-tank-from-ghost-in-the-shell-brought-to-life/)。休息后的视频。

【感谢 Baldpower 的提示！]

 [https://www.youtube.com/embed/bmoGfBe63ZA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bmoGfBe63ZA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

