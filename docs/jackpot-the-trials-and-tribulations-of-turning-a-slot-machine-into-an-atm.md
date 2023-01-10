# 头奖！:把老虎机变成自动取款机的考验和磨难

> 原文：<https://hackaday.com/2019/11/21/jackpot-the-trials-and-tribulations-of-turning-a-slot-machine-into-an-atm/>

你曾经希望老虎机像自动取款机一样容易分发钱吗？《奇异零件》的斯科特·艾伦(Scotty Allen)也是如此，所以他和他的朋友马特(Matt)决定将两者结合起来。在充满魔法烟雾和挫折的四个月旅程后，他们设法建造了一台功能齐全的自动取款机。

基本的想法是，你插入你的卡，像在普通的自动取款机上一样输入你的密码，选择你的中奖金额，然后拉杠杆。这使轮子旋转，每次都是三个一类的轮子停下来，你赢得了你自己的钱，作为一桶硬币，伴随着所有的宣传。这个项目花费的时间比[Scotty]预计的要长，结果他错过了在 DEF CON 上展示这台机器的原定截止日期。

他们从一台破旧的日本老虎机开始，经过大量的逆向工程和黑客攻击，用 Arduino 取代了控制板。[Scotty]做了一个很酷的视频，就在[让原来的真空荧光显示屏工作](https://www.youtube.com/watch?v=cy6o8TrDUFU)。事实证明，集成 ATM 部件是最大的挑战，许多非常昂贵的部件在这个过程中会释放出神奇的烟雾或被烧坏。[Scotty]想出了一个巧妙简单的方法来连接 ATM 硬件和 Arduino。现金纸币分发器使用多个传感器来检测是否装载了纸币以及是否成功分发了一张纸币。这些都是 Arduino 欺骗的，它控制两个硬币漏斗，而不是分发适量的硬币或便士。玻璃面板上的一些非常整洁的自定义图形使该构建更加完美，该机器最终在当地的一个拱廊展示。

这是一个令人敬畏的项目，我们可以欣赏这样一个事实，即[Scotty]没有试图隐藏真正的情感过山车，任何从事大型项目的人都知道这一点，但很少记录在日志中。[Scotty]通过用零件组装自己的 iPhone 和[参观深圳的许多工厂](https://hackaday.com/2018/06/12/scotty-allens-pcb-fab-tour-is-like-willy-wonkas-for-hardware-geeks/)而出名。休息之后看看视频

 [https://www.youtube.com/embed/nHDpzczgdo0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nHDpzczgdo0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/QIuVINz4lFQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QIuVINz4lFQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

