# 示波器软件的物理前面板

> 原文：<https://hackaday.com/2021/01/28/a-physical-front-panel-for-oscilloscope-software/>

对于预算紧张或工作台空间有限的黑客来说，USB 示波器可能是专用硬件的令人信服的替代品。对于许多爱好者来说，这是一个完全有效的选择。但是，虽然关于这些设备的利弊的更大讨论最好留到另一天进行，但当你的示波器界面是一个软件时，有一件事你肯定会错过:物理按钮和旋钮的感觉。

但是如果事情不一定是那样呢？[保罗·威瑟斯(Paul Withers)的 ScopeKeypad 在使用虚拟界面时，看起来像一个漂亮的台式示波器。这样的装置真的有必要吗？不，当然不是。虽然有人可能会说，与拖动屏幕上的滑块相比，通过旋转编码器上的棘爪旋转会获得一定的反馈优势。把它想象成一个飞行模拟器的按钮盒:当然你可以只用键盘和鼠标来驾驶飞机，但是你会有一个更好的界面。](https://github.com/PaulusSmallus/ScopeKeypad)

与飞行模拟器面板的比较实际上更深入一点，因为这本质上就是 ScopeKeypad。随着 STM 32“Blue Pill”微控制器对 USB 人机界面设备的最佳印象，当旋转适当的编码器或按下按钮时，面板会发出指定的虚拟按键。该项目的设计考虑到了 PicoScope，甚至包括一个方便的键映射文件，您可以直接将其加载到程序中，但它肯定可以与其他软件包一起使用。如果你愿意的话，它甚至可以在*克巴尔太空计划* 中充当你的虚拟飞船的[控制器。](https://hackaday.com/2018/01/23/building-a-better-kerbal-space-program-controller/)

负担得起的 USB 示波器[已经走过了漫长的岁月](https://hackaday.com/2016/10/06/open-design-oscilloscope-could-be-almost-free/)，如今，使用一个示波器已经不再是过去的耻辱。但是经典长凳瞄准镜的[外观和感觉就像它得到的](https://hackaday.com/2019/09/10/digital-oscilloscope-does-its-best-analog-impression/)一样永恒，所以我们当然可以看到一个试图结合两个世界最好的项目的吸引力。

 [https://www.youtube.com/embed/zDIKAT928zg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zDIKAT928zg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

