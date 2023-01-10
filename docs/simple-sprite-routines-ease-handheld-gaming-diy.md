# 简单的精灵例程简化手持游戏 DIY

> 原文：<https://hackaday.com/2020/05/26/simple-sprite-routines-ease-handheld-gaming-diy/>

使用[戴维·约翰逊-戴维斯][Adafruit py badge 和 PyGamer boards](http://www.technoblogy.com/show?33W0) 的简单精灵例程，制作自己的手持游戏变得更加容易。精灵可以被认为是小的、固定大小的图形对象，可以被绘制、擦除、移动并检查与其他屏幕元素的冲突。

`![](img/355f062e61c5fbaa844ee19dd6a2d074.png)xorSprite()`绘制一个 8×8 的精灵，`moveSprite()`将给定的精灵移动一个像素而没有任何闪烁，`hitSprite()`检查一个精灵是否与给定颜色的任何屏幕元素冲突。这就是实现一个简单游戏所需要的全部，而且[大卫]使它们易于使用，甚至以这里所示的滚球迷宫的形式为[提供了一个演示程序](http://www.technoblogy.com/list?354F)。

这些例程可以与 PyBadge 和 PyGamer 一起使用，但应该很容易适应任何基于 ST7735 控制器的 TFT 显示器。PyGamer 是这里显示的板子，但是您可以看到 [PyBadge，因为它被用来创建一个支持 MQTT 的会议徽章](https://hackaday.com/2020/02/18/mqtt-and-the-internet-of-conference-badges/)。

如果你真的想进入基于 sprite 的游戏图形的兔子洞，你绝对不能错过听到内置在 FPGA 游戏男孩徽章中的系统【Sprite_TM】。