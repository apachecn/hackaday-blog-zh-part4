# 到处都是电子鸡

> 原文：<https://hackaday.com/2021/08/10/tamagotchis-everywhere/>

电子鸡相对简单的技术复杂性与其巨大的文化影响力相比相形见绌，售出了 7600 多万只。它催生了漫画、故事、无数的玩具和分支，如一部动画和两部电影。[JC]正在翻他的一些旧东西，偶然发现了一只电子鸡 P1(原来的电子鸡)，于是[决定为它制作一个便携式模拟器](http://blog.rona.fr/post/2021/08/04/Spreading-virtual-life-everywhere)。P1 的 ROM 早已被抛弃，可以在 MAME 模拟器中运行。毕竟，它只是一个 32MHZ 的 E0C6S46 爱普生 MCU，32×16 LCD，8 个附加图标，三个按钮和一个压电。MCU 的手册甚至可以在[爱普生的网站](https://download.epson-europe.com/pub/electronics-de/asmic/4bit/62family/technicalmanual/tm_6s46.pdf)上找到。在 Hackaday，我们以前已经见过很多次电子鸡，例如[电子鸡奇点的无限矩阵](https://hackaday.com/2015/11/24/building-the-infinite-matrix-of-tamagotchis/)和基于 6502 内核的最新一代电子鸡的 ROM 转储[。](https://hackaday.com/2013/05/24/tamagotchi-rom-dump-and-reverse-engineering/)

那么[JC]试图实现的目标有什么不同呢？首先，工具。它分为两部分:TamaLIB 和 TamaTool。第一个是硬件无关的 P1 仿真库，它依靠 HAL 层与硬件通信。第二个是第一个的前端，允许调试、RAM 编辑和修改 ROM。特别是，它支持轻松修改 ROM 中的图像，并允许定制鸡蛋和电子鸡。向快乐扳手致敬很好。

假设仿真是平台无关的，并且不能保证对低分辨率定时器的访问，那么周期计数就变得很棘手。[JC]偶然发现的相当聪明的解决方案是同步输入轮询、屏幕更新和声音输出。TamaLIb 跟踪已经过了多少 CPU 周期，并定期检查仿真是否进行得太快或太慢。减慢或加快模拟速度可以让它看起来像是实时运行的。

[JC]的最终目标是在嵌入式硬件上运行它。使用 STM32F072 板和廉价的有机发光二极管屏幕制作了一个便携式仿真电子鸡，称为 MCUGotchi。GitHub 上提供了[代码，只要稍加调整，就可以在大多数 STM32 MCUs 上运行。既然有人已经努力让在任何地方经营电子鸡变得简单，也许用不了多久，我们就会看到咖啡机或智能灯充当电子鸡。也许新的笑话会是，它能运行电子鸡吗？](https://github.com/jcrona/mcugotchi)

休息后的视频。

 [https://www.youtube.com/embed/ZgO-gPx6IZI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZgO-gPx6IZI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Jean-Christophe Rona]发送这封邮件！