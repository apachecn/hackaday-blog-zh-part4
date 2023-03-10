# 射频遥控器不是逻辑分析仪的对手！

> 原文：<https://hackaday.com/2021/09/16/an-rf-remote-is-no-match-for-a-logic-analyser/>

Neewer NL660-2.4 视频键盘灯有一个方便的遥控器，对于[Tom Clement]来说，它有一个重大缺陷，即它无法将灯光恢复到上次通电时的状态。因此，他不厌其烦地对其进行逆向工程，并使用一个配备合适的 Arduino 克隆体创建了自己的遥控器。

这篇文章是潜在的射频远程黑客的入门指南，在试图转储 STM8 的固件之前，将大脑识别为 STM8，将无线电识别为 NRF24 克隆。正如预期的那样，STM 是受保护的，只剩下嗅探两个芯片之间连接的选项。SPI 引脚由逻辑分析仪适时探测，并提取 Neweer 使用的代码。幸运的是，有一种叫做 RF Nano 的便利板，它是 Arduino Nano 和 NRF24 的 Arduino Nano 外形，因此概念验证遥控器可以写在一体化模块上。如果你好奇的话，你可以在 GitHub Gist 中找到结果[。](https://gist.github.com/tjclement/2deaa87c48a04812aba883d9f56f5824)

我们以前见过 Tom 几次，特别是在他的欧洲 BadgeLife 工作中，作为其中的一部分，他付出了很多努力，将基于浏览器的 WebUSB 和 WebSerial 开发融入到他的工作中。