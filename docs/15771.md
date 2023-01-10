# 旋转全息 POV 死亡圣诞树

> 原文：<https://hackaday.com/2022/12/27/spinning-holographic-pov-christmas-tree-of-death/>

[肖恩·哈金斯]真正利用节日精神创造了他自己的[巨型旋转全息圣诞树](https://www.instructables.com/Giant-Spinning-Holographic-Christmas-Tree-Display/)(死亡)。这是一个三维视觉暂留(POV)杰作，但作为快速旋转的金属元素的集合，它也有潜在的危险。正如[Sean]所展示的，该系统可以显示其他图像和动画，远远超出了仅仅是假日树的范畴。

最初的实验侧重于改进机械结构、轴承和电机。选择 1/2 马力的交流电机，然后“修剪”树的尺寸，以优化三角形框架，该框架可以通过结实的电机以必要的 POV 速度旋转。六线电滑环允许电力和控制信号通过旋转的中心轴耦合到采油树。

RGB 元素是 SK9888 LEDs，也称为点星 led。点星 led 是可串联、可单独寻址的 RGB LEDs，类似于 NeoPixels。然而，由于脉冲宽度调制(PWM)速率约为 50 倍，DotStars 比 NeoPixels 更适合 POV 应用。LED 链由 Raspberry Pi 4 单板计算机驱动，使用智能系统存储图像帧。

如果致命的旋转速度不符合你的胃口，考虑一下这个旋转速度较慢的 RGB 圣诞树，它有一个 DIY 滑环。或者对于更多的观点，我们可以建议这种[极简视觉暂留显示器](https://hackaday.com/2022/11/09/1-pov-display-goes-round-and-round/)，只需要几个 led 和一个 ATtiny CPU。

 [https://www.youtube.com/embed/-R5Wl697IuM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-R5Wl697IuM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

