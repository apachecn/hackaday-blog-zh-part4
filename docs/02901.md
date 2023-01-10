# 在晶体管测试仪上玩俄罗斯方块，因为为什么不呢？

> 原文：<https://hackaday.com/2019/05/03/play-tetris-on-a-transistor-tester-because-why-not/>

[罗布森]从 15 岁起就一直使用同一台万用表。它也不是典型的万用表。他已经将它编程为也可以玩谷歌 Chrome 跳跃恐龙游戏，并且还在各种会议上将其用作徽章。但由于所有这些弊端，带状电缆断了，他开始着手其他项目。就像这个[晶体管测试仪，它只是要求将俄罗斯方块编程](https://dragaosemchama.com/en/2019/04/gm328a-reverse-engineering-new-firmware-and-tetris/)到它的小屏幕上。

晶体管测试仪是为各种晶体管测试应用而制造的 GM328A，但也是一种 LCR 计。[罗布森]的旧电表甚至没有测试电容，但他能够使用多年，所以这个设备应该更好地为他服务。一旦交付，他就开始添加更多的功能，即俄罗斯方块。它基于 ATmega 芯片，非常容易使用(这是你在 Arduino Uno 中找到的同一芯片，但[罗布森]走了 Makefile 路线，而不是旋转 IDE)。他不仅添加了更多的功能，还在频率计数器电路中发现了一个错误，并在项目过程中自行修复了这个错误。

如果你一直认为你的万用表缺少游戏是一个总的交易破坏者，这个项目值得一读。即使你只是随便放了一个基于某种 ATmega 芯片的设备，这也是让这个设备做其他事情的良好开端。这种情况在也很常见。

 [https://www.youtube.com/embed/-8niuGSMips?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-8niuGSMips?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

