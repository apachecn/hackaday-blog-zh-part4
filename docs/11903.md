# 小护身符警告佩戴者紫外线暴露

> 原文：<https://hackaday.com/2021/11/14/tiny-talisman-warns-wearer-about-uv-exposure/>

鉴于我们的太阳是如此重要，我们的祖先将其视为神是可以原谅的。即使现在我们知道它实际上是什么，它是如何工作的，也没有理由认为太阳会释放出邪恶的灵魂，这些灵魂会给那些晒太阳太久的人带来疾病和死亡。所以[一个抵御邪恶紫外线的护身符](https://mitxela.com/projects/amulet)是一个完全合理的项目，对吗？

正如[mitxela]的项目经常出现的情况，尤其是[那些更令人眼花缭乱的项目](https://hackaday.com/2017/02/12/tiny-led-earrings-are-a-miniaturization-tour-de-force/)，这个项目几乎是电子和精细金属加工的对等部分。下面的大部分视频集中在金属制品上，这是非常有趣的东西。护身符的外壳由黄铜制成，大小适合 CR2032 硬币电池。护身符的背面有螺纹作为电池盖，那里需要一些花哨的车床加工。表壳还电镀了黄金，以防止失去光泽，并在与 PCB 的黑色阻焊膜搭配时提供了一个漂亮的外观。

在电子设备方面，[mitxela]努力将电池消耗保持在尽可能低的水平，并充分利用可用空间，选择 ATtiny84 来支持 TTP223 电容检测芯片和 VEML6075 UV 传感器。触摸传感器允许佩戴者唤醒护身符，并通过紫外线模式循环,[mitxela]了解到这并不完全是传感器数据表上所说的那样。这需要一些软件破解，但最终，护身符在报告紫外线指数方面做得很好，而且看起来棒极了。

 [https://www.youtube.com/embed/JhNMeJZ8Ll0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JhNMeJZ8Ll0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

