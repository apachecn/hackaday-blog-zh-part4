# 长号控制虚拟长号

> 原文：<https://hackaday.com/2022/09/27/trombone-controls-virtual-trombone/>

吉他英雄是十几年前的一种文化现象，它表明在控制器上演奏虚拟乐器是一件非常有趣的事情。现在还有其他几个类似的游戏可以用于不同的乐器，包括一个名为长号冠军的游戏，洪(Hung Truong)是这个游戏的粉丝，它用长号取代了传统的吉他。长号的滑动动作明显不同于吉他的品音，这使它成为视频游戏中一个独特的挑战。但是一个额外的挑战是为游戏制作一个控制器，通过演奏一个真正的长号来工作。

与可以轻松将手指位置映射到按钮的吉他不同，将长号这样的模拟乐器及其连续滑动映射到数字空间要困难一些。这里的方法是使用 ESP32，并对其进行编程，以将鼠标输入发送到计算机。首先，一个气压传感器被添加到长号的铃上，这样当空气通过它时，鼠标的点击就会被记录下来，这告诉计算机当前正在演奏一个音符。第二，通过使用也安装在铃上的飞行时间传感器，由滑块的位置产生鼠标位置。ESP32 将这些鼠标信号发送到计算机，然后用作游戏的输入。

虽然[Hung Truong]发现他的传感器不是最高质量的，但他确实发现控制接口的延迟和控制接口本身相对成功。通过对传感器进行一些调整，他认为这可能是一个比目前原型更有效的设备。如果你想知道是否存在类似的吉他英雄，请看一下这个来自 09 年的经典作品。

 [https://www.youtube.com/embed/lUXrkq2e1zk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lUXrkq2e1zk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

