# 按钮推进器自动完成动物穿越任务

> 原文：<https://hackaday.com/2021/03/05/buttonpusher-automates-animal-crossing-tasks/>

按下按钮，等待，再次按下按钮，重复。一定有更好的办法！如果这种互动让你抓狂，你可能会喜欢[汤米]的[按钮按钮](https://blog.tommy.sh/posts/buttonpusher/)，它只有一个任务:自动化掉任天堂*动物穿越*中一些更无聊的部分。一方面，这款设备的工作非常简单:按下任天堂游戏机上一个预设模式的按钮。没有反馈循环，它只是默默按下并等待。但是这个版本仍然有一些有趣的地方。

[![](img/7fd1244f9dd40580395456a8b9d01558.png)](https://hackaday.com/wp-content/uploads/2021/03/buttonpusher-pushing-anim.gif)

Rigid mounting combined with interfacing the actuator to the servo horn (instead of to the servo shaft) were the keys to reliable button pushing.

首先，[汤米]发现小 9g 遥控伺服可以可靠地施加足够的力来按下 joy-con 上带有正确适配器的按钮。他认为，如果没有更大的机械优势，伺服系统会太弱，无法完成这项工作，但一个简单的锤子式致动器可以轻松完成这项工作。好吧，只要伺服和 joy-con 被严格控制，它就能做到；他的第一个版本在部件的握持方面允许有太多的摆动，按钮按压也没有完全记录下来。有了一个 3D 打印的夹具来刚性地安装伺服和 joy-con，事情就好了。

在制作 buttonpusher 的过程中，使用了[circuit python](https://circuitpython.org/),【Tommy】创建了一个工具来自动化他正在运行的另一个讨厌的任务: [circuitpython_tools](https://github.com/rocktronica/circuitpython_tools) 被创建来自动监视代码变化，转换。将文件复制到(较小的)MicroPython 字节码中。mpy 文件，然后自动部署到板上。这在开发过程中为[Tommy]节省了大量时间和麻烦，但这是必要的，因为他很快就用完了 M0 Metro Express 板上的内存，并且无法以任何其他方式适应他的代码。

不过，这是一个很好的例子，说明一个项目有时会衍生出其他项目，并导致各种各样的经验教训。在下面的视频中，你可以看到 buttonpusher 自动完成了动物穿越的制作过程。

[https://player.vimeo.com/video/427842316](https://player.vimeo.com/video/427842316)

视频游戏控制器自动化是一个常见的项目，尤其是非破坏性黑客。人们变得相当有创造力，[甚至想出了自动化操纵杆移动的方法](https://hackaday.com/2020/04/24/automate-your-xbox/)。