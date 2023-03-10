# 西蒙说，硅胶拍打伺服解决

> 原文：<https://hackaday.com/2022/12/06/silicone-slapping-servos-solve-simon-says/>

大多数现代电脑游戏都有一个明确的结尾，但许多经典游戏，如《吃豆人》和《T2》中的《猎鸭》可以无限期地继续下去，只受技术限制，如内存大小。有人会认为经典的电子记忆游戏*西蒙*也应该属于这一类，但是大多数人甚至都在努力达到 20 级，这很难确定。[迈克尔·舒巴特]决心找出西蒙的最新化身是否真的有尽头，并制造了一个机器人来帮助他的探索。

[![](img/0d64926a2c5dc44cdd3813783cee23b1.png)](https://hackaday.com/wp-content/uploads/2022/12/simon_detail.jpg)*西蒙·艾尔*，作为已知的最新版本，使用运动传感器来检测手部运动，实现无触摸游戏。[迈克尔]因此做了一个系统，用伺服驱动的硅树脂手拍打运动传感器。游戏产生的音调序列被光敏电阻检测到，光敏电阻感知哪个部分被点亮；Raspberry Pi 跟踪序列，并通过驱动伺服系统重放它。

我们不会破坏结局，但[迈克尔]确实找到了他的问题的答案。游戏的早期版本已经在 Arduino 的帮助下进行了测试，尽管它显然不够快，无法将游戏推向极限。如果你认为*西蒙*可以改进，你可以随时[推出自己的](https://hackaday.com/2019/07/12/simple-simon-says-looks-sharp/)，无论是从头开始还是通过[改装现有的玩具](https://hackaday.com/2012/11/04/hacked-farm-toy-plays-simon/)。

 [https://www.youtube.com/embed/q3dD5nk04J4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/q3dD5nk04J4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

