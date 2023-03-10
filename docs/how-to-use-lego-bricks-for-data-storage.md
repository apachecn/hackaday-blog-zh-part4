# 如何使用乐高积木进行数据存储

> 原文：<https://hackaday.com/2022/06/06/how-to-use-lego-bricks-for-data-storage/>

那些年纪足够大，一生中遇到过穿孔卡片的人可能很高兴摆脱它们极低的数据密度和高高的书库翻倒的倾向。尽管它们可能已经过时，但它们是展示二进制数据存储基础的一个很好的工具:这些位很容易看到，甚至可以用简单的工具来操作。作为在更现代的系统中重现这些功能的实验，[Michael Kohn]基于乐高积木制作了一个类似穿孔卡的系统，为 65C816 CPU 存储机器代码指令，65c 816 CPU 是古老的 6502 的 16 位继任者。

比特存储在一个白色的 8×20 钉板上，上面放着黑色的小块。白色背景螺柱编码逻辑“0”，而黑色螺柱编码逻辑“1”。这些位由反射传感器阵列读取，该阵列方便地具有与标准乐高钉相同的 8 毫米间距。一个由步进电机驱动的大轮子沿着一小段乐高火车轨道在读出电路下滑动数据卡。

光学传感器由 MSP430 系列微控制器读取，该微控制器还通过步进电机驱动器驱动电机。一旦数据被读出，字节被传送到 WDC W65C265SXB 板，该板在其 65C816 CPU 上将它们作为机器代码指令执行。在下面的视频中，你可以看到一个程序正在加载，闪烁的 LED 灯。

我们以前也推出过教育打卡系统，比如[这个基于 Raspberry Pi 的模型](https://hackaday.com/2016/02/22/punch-card-reader-for-the-10-types-of-people-in-the-world/)。如果你有一堆需要读出的实际穿孔卡，看看[这个 Arduino 供电的读出系统](https://hackaday.com/2015/01/17/arduino-reads-punch-cards/)。

 [https://www.youtube.com/embed/PTmaIfTDryk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PTmaIfTDryk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

