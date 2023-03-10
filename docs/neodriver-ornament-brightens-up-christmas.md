# Neodriver 饰品点亮圣诞

> 原文：<https://hackaday.com/2022/10/21/neodriver-ornament-brightens-up-christmas/>

商店会卖给你各种各样华而不实的节日装饰品，但是没有什么能比得上你自己制作的装饰品的风格和档次。[w3arycod3r]就是这么做的，[制造出有趣而喜庆的 Neodriver 装饰品。](https://github.com/w3arycod3r/neodriver-ornament)

这是一个电池供电的建筑，使用可充电的 18650 电池，在低占空比下提供几天的运行。ATtiny85 负责向各种新像素设备发送命令，从环形到矩形阵列。[w3arycod3r]然后设计了各种 PCB，可以在一个平衡的包装中携带硬件和电池，当挂在圣诞树上的丝带上时，会很好地悬挂。

作为可寻址 led 的有趣部分，[w3arycod3r]创造了一些有趣的动画来适应。新像素的 5×5 矩形阵列能够提供滚动文本，而另一个动画则显示了每个人最不喜欢的冠状病毒新型冠状病毒的 RNA 序列。让一切都适合 ATtiny85 的 8 KB 代码空间和 512 字节 EEPROM 是一个挑战，但精简 Adafruit NeoPixel 库并使用直接 AVR 寄存器操作代替常规 Arduino 功能有所帮助。

总的来说，这是一个有趣的节日建筑，在树上看起来很棒。或者，考虑在这个假期给自己做一些[流变饰品](https://hackaday.com/2020/12/27/rheoscopic-holiday-ornaments/)。而且，如果你已经有了自己的有趣的假期计划，[把它扔到网上吧！](https://hackaday.com/submit-a-tip)