# 经典放大器以圆周率复活

> 原文：<https://hackaday.com/2022/07/05/classic-amp-revived-with-a-pi/>

吉他放大器的寿命很长，正如任何经营过场地的人都会告诉你的那样，在经历了旅途生活后，它们经常会遇到严重的电气问题。[Dsagman]有一个内部受损的 Vox 放大器，他没有修复原来的放大器，而是用树莓 Pi 内部进行了重建，以提供一系列满载的效果。

虽然主题是 Vox，但最好将其视为如何在 Pi 中创建吉他效果数组的故事，而不是将其放入放大器中。Pi 有一个音频板和一个 MCP3008 ADC，利用这两个器件，它从一系列电位计获取输入，并处理通过音频板的音频。此外，还有一系列 LED 指示灯和一个 LED 条形图，让用户随时了解正在发生的事情。

所有这些都很好地集成在 VOX 外壳中，所有电位计都在一个铝板上。他讨论了放大器的选择，但正如你所料，最终选择是 D 类模块。总之，许多读者可能会去的放大器。

长期读者会记得，[吉他效果器在这里出现过几次](https://hackaday.com/2018/05/08/stomping-microcontrollers-arduino-mega-guitar-effects-pedal/)。

 [https://www.youtube.com/embed/wl24fLW1fQE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wl24fLW1fQE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

