# 在你的口袋里放一个 ItsyBitsy Zork

> 原文：<https://hackaday.com/2018/11/08/put-an-itsybitsy-zork-in-your-pocket/>

在电脑游戏拥有这些花哨的图形之前，基于文本的游戏是一种非常流行的类型。你不用移动屏幕上的角色，而是以游戏可以解释的句子形式为你的玩家输入命令；比亚马逊和谷歌等公司目前用于虚拟助手的“云”语言处理技术早几十年。在某些方面，这种风格是超前的，但是它没有在家用电脑的图形革命中幸存下来。当然，这些游戏仍然有一些铁杆粉丝。

[![](img/543fe797dabea3fe6246f394e356040d.png)【丹那怪胎】T2 就是这样一个粉丝。他非常喜欢像 Zork 这样的基于文本的冒险游戏，以至于他](https://hackaday.com/wp-content/uploads/2018/11/a2z_thumb.jpg)[想要创建自己的核心技术](http://danthegeek.com/2018/10/30/a2z-machine-running-zork-on-an-adafruit-itsybitsy-m4-express/)的实现，这些核心技术在多年前使这些游戏成为可能。但他不想只在这台台式电脑上做，已经有项目让你在现代硬件上运行这些经典游戏。他想看看他是否可以在现代微控制器上运行这些经典游戏，并在一个方便的便携式设备上创建一个真实的复古体验。

[Dan]首先解释了在种类繁多的家用电脑需要细致入微的方法的时代，用来制作这些标题的技术。通过将故事文件从实际的解释程序中分离出来，开发者可以更容易地将游戏移植到不同的计算机上。理论上，这些被称为“Z-machines”的解释器可以为任何能编译 C 代码、有足够的内存来存储故事、有终端和键盘的计算机编写。这不完全是我们习惯看到的现代电脑游戏的系统要求，但这是在 1980 年代。

理论上，一个现代的微控制器将满足这些要求，所以[丹]想创造一个他自己的 Z 机器。但他不想像以前的 Arduino Z-machine 那样使用 SD 卡“作弊”，而是想看看是否有一种开发板可以在内部完成这一切。答案来自于 Adafruit ItsyBitsy M4 Express，它拥有 192 kB 的内存和 2 MB 的 SPI 闪存。

由[Dan]创建的 Z-machine，他称之为 A2Z，允许用户在 ItsyBitsy 上运行 Zork 和其他兼容的交互式文本游戏，而无需任何额外的硬件。只要把这个板插到你的电脑上，你就可以通过串行连接玩游戏了。他甚至实施了一些复古的配色方案，让体验更加真实，比如 Amiga 的蓝色或 Compaq 的绿色。

我们已经涵盖了之前的项目，这些项目[将 Zork 和朋友带到 Arduino](https://hackaday.com/2014/04/30/the-zorkduino/) ，通过虚拟的 Altair 8800 将你的[网络浏览器，甚至一些](https://hackaday.com/2014/12/12/online-altair-8800-clone-lets-you-play-zork/)[更奇特的目标，如定制 FPGA](https://hackaday.com/2017/02/21/zork-comes-to-custom-fpga-cpu-again/)。你可以在超级徽章上玩《洞穴探险》,这款游戏启发了佐克。