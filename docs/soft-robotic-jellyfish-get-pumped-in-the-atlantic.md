# 柔软的机器水母在大西洋里抽水

> 原文：<https://hackaday.com/2018/10/06/soft-robotic-jellyfish-get-pumped-in-the-atlantic/>

在最近发表在*生物灵感&仿生学* 的一篇论文中，佛罗里达大西洋大学的研究人员描述了建造和测试五只自由游动的软体机器水母的过程。这篇论文包含了三个不同变量——触手硬度、划水频率和划水幅度——如何影响每个机器人游泳特性的构建细节和数据。对于更深入的构建日志，我们发现[Jennifer Frame 的原始硕士论文](https://fau.digital.flvc.org/islandora/object/fau%3A33675/datastream/OBJ/view/Self-Contained_Soft_Robotic_Jellyfish_with_Water-Filled_Bending_Actuators_and_Positional_Feedback_Control.pdf)非常*全面，包括流程、原理图、零件清单，甚至一些 Arduino 代码。*

尽管旱鸭子可能会说这些机器人看起来更像一只矮胖的章鱼，而不是水母，但根据这篇论文，它们的形状实际上最类似于幼年的“ephyra 阶段”月亮水母，有 8 条短触角从中心身体辐射出来。柔性触手由 Smooth-On 的硅橡胶材料制成，并在 3D 打印模具中铸造而成。防水主体内部是一个 [Teensy 3.2](https://www.pjrc.com/teensy/) 微控制器、一些闪存、一个九轴 IMU、一个温度传感器和一个 9 V 电池。

身体中嵌入了两个柔性电阻来测量触手的弯曲，实际的弯曲是通过将海水泵入触手中的开路液压通道来完成的。两个 3 V 迷你泵足以进行泵送，开路意味着当泵关闭时，触角排出任何剩余的压力，并迅速恢复到它们的“中立”位置，而无需使用复杂的阀门。

另一个简单的功能是两个霍尔效应传感器，安装在机身上，以实现与微控制器的防水“无线通信”。选择无线协议:手动在传感器上挥动磁铁，让机器人在几个预先定义的操作模式之间切换。

休息后有一个舒缓的，有气氛的视频，你可以看到机器人在佛罗里达海岸活动。

 [https://www.youtube.com/embed/Aaugq16rCAw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Aaugq16rCAw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



有水母吗？我们之前报道过一个[氢动力水母机器人](https://hackaday.com/2012/03/22/robot-jellyfish-fueled-by-hydrogen-from-the-water-around-it/)，和一个[六角机器人“陆地水母”](https://hackaday.com/2011/12/12/sphere-morphing-hexabot-is-a-mechanical-jellyfish/)。

感谢[baldpower]的提示。