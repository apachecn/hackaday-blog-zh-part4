# RC Strandbeest 比其他人高出一头

> 原文：<https://hackaday.com/2019/12/08/rc-strandbeest-is-a-head-above-the-rest/>

多产的制造商[杰里米·库克]最近对他令人印象深刻的 ClearCrawler 遥控 strand beest 进行了最后的润色(至少目前如此)，其中包括一个令人惊讶的富有表现力的“头部”，配有 led 矩阵眼睛。对于之前只对这些多足机器人感到轻微恐惧的观众来说，休息过后，你可能想把目光从视频上移开。

被称为 Strandbeest 的[Theo Jansen]巧妙的机车设计是一种腿式步行器。它的特别之处在于，腿本身不是独立的，而是协同工作，进行更类似于有轮子的机器人的滑行动作。[Jeremy]与 ClearCrawler 的合作已经将这种精确和机械化提升到了另一个水平。

[![](img/6e55a4cd07fe72d7fe5208e26e8eecdb.png)](https://hackaday.com/wp-content/uploads/2019/12/clearcrawler_detail.jpg) 在安装电子设备之前，ClearCrawler 必须拴在一个工作台电源上，只能前后移动。一旦运动如预期的那样工作了，[杰里米]就准备给这头野兽安装一些大脑。

机器人由双电机驱动器和插入 I/O 扩展板的 Arduino Nano 控制。助行器上的 Nano 和手持遥控器之间的通信由一对 nRF24L01 模块提供。控制器本身很简单，由一个插入 Arduino Uno 的操纵杆护罩组成。

机器人的头部由一大块透明的聚碳酸酯管组成，内部框架由 3D 打印而成，用于容纳双 8×8 LED 矩阵，作为其动画眼睛。这种布置安装在伺服云台上，由控制器上的模拟杆控制。虽然头部目前没有任何实际功能，但它确实给了[杰里米]一个机会来表达他的创作；这是他展示 ClearCrawler 时常用的伎俩。

几年前，我们报道了这款机器人的前身[更大的 ClearWalker](https://hackaday.com/2017/06/01/watch-the-clearwalker-light-up-and-dip-its-toes/) 。虽然这台机器看起来确实很漂亮，但这个更小、更灵活的概念更实用。

 [https://www.youtube.com/embed/ZRGWC96ruIg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZRGWC96ruIg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

