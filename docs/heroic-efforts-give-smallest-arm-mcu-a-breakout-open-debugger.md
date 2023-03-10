# 英勇的努力给最小的 ARM 微控制器一个突破，开放调试器

> 原文：<https://hackaday.com/2022/03/21/heroic-efforts-give-smallest-arm-mcu-a-breakout-open-debugger/>

在今天这一集的小型设备技术概述中，[Sprite_TM]又来了——这一次[征服了 HC32L110](https://spritesmods.com/?art=hc32l110&f=had) 。几周前，[我们重点介绍了](https://hackaday.com/2022/03/01/new-part-day-smallest-arm-mcu-uproots-competition-needs-research/)小型 ARM Cortex M0+微控制器，它的出色之处在于其异常小的尺寸。我们还指出了一些障碍，其中包括难以接近的 SDK 和文档，以及为如此小的 BGA 制作和组装 PCB 的困难。今天，我们见证了[Sprite_TM]如何为我们所有人克服所有这些障碍，并在我们的集体“令人发指的焊接”画廊中添加了一些图片。

首先，他[为这款 MCU 设计了一个示例布局](https://spritesmods.com/?art=hc32l110&page=2&f=had),我们甚至可以在 JLCPCB 最便宜的两层板上实现，通过去掉几个引脚将距离保持在通用容差标准内。因此，我们只失去了对四个 GPIOs 的访问——这些 GPIOs 必须作为输入保留，这样就不会烧毁任何东西。然而，如果这有助于我们保持 PCB 的小巧轻便，以满足这些因素至关重要的项目需求，那么这种权衡是可以接受的。收到制作好的电路板后，他还为[录制了一个简短的教程](https://www.youtube.com/watch?v=wOE9K0gox3E)，讲述如何在家里用热风枪和一些像焊剂和镊子这样的必需品焊接这样的封装——嵌入在下面。

然而，事情并没有就此结束，因为他决定以一种意想不到的方式解决 GPIO 扇出限制。显然，[Sprite_TM]决定找点乐子，拿一块 0.1 英寸间距的常规原型板，用磁线堵住芯片，这让我们很开心。最终的装置，如上图所示，起作用了——这是你希望在急需的时候能够实现的事情，无论你是通过使用一种受诅咒的安装技术来工作还是仅仅为了娱乐，有一个长达一小时的直播记录了这个磁线装置是如何产生的。当然，这并不是最后要分享的东西。

作为点睛之笔，他为华大 SDK 发布了[绑定和包装，这样芯片就可以用于 GCC、GDB 和 OpenOCD。他还](https://github.com/Spritetm/hc32l110-gcc-sdk)[将数据表添加到同一个存储库](https://github.com/Spritetm/hc32l110-gcc-sdk/tree/master/translated_docs)——自动翻译，但可读性很强。一个磁线绑定芯片的全 GPIOs 参与 blinkie GIF 胜利地[结束了写](https://spritesmods.com/?art=hc32l110&page=3&f=had)。

[Sprite_TM]工具包的增加就是每个人工具包的增加——技术、见解和资源都在这里供我们学习。如果你曾经怀疑过自己处理小封装的能力，特别是这个 MCU，现在你有更多的材料可以利用了！

想知道你想做什么样的微型装置？到目前为止，我们黑客大部分时间都在找乐子，建造像隐藏 USB 电缆的橡皮包或 T2 微型等离子显示器这样的东西，但是在可穿戴设备或医疗领域，这样一个小的微控制器肯定会成为黑客的朋友。也许你想为[打造一枚带有 Cortex-M0+智能的 LED 订婚戒指](https://hackaday.com/2013/05/20/adding-leds-to-an-engagement-ring/)？事实上，这个微控制器足够小，以至于将[隐藏在你的 PCB](https://hackaday.com/2019/01/18/oreo-construction-hiding-your-components-inside-the-pcb/) 本身中并不困难。

 [https://www.youtube.com/embed/wOE9K0gox3E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wOE9K0gox3E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

