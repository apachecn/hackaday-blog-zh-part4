# 超级徽章硬件黑客:这里有什么要带

> 原文：<https://hackaday.com/2018/10/25/supercon-badge-hardware-hacking-heres-what-to-bring/>

Hackaday Superconference 离我们只有一周的时间了([珍贵的几张票还剩下](https://www.eventbrite.com/e/hackaday-superconference-2018-tickets-47386813234?aff=1025com))，这是一场 Hackaday 所有事情的庆典，其中自然包括充分利用硬件的创意项目。每个与会者都以[会议徽章](https://hackaday.io/project/161859-2018-hackaday-superconference-badge)的形式获得一个黑客平台。

为了让你的徽章黑客乐趣最大化，提前计划，这样你会有额外的组件和你需要的工具。最基本的是，**带上一根串行转 USB 线和一个 PIC 编程器**。这些都是常见的，如果你没有，问问周围的人，你可能会借他们。现在也是**为您想要使用但手头没有的任何组件下零件订单**的时候了！

这个徽章是可以破解的，没有任何额外的东西，但它是为添加硬件和破解固件而设计的。我们很想知道你能用它做什么。几天前，我们向[介绍了这款复古主题袖珍电脑的概况](https://hackaday.com/2018/10/17/the-supercon-badge-is-a-freakin-computer/)，今天，我们邀请您为您的硬件黑客开发其潜力。

## 扩展接头、板和定制固件

[![](img/af8d300f87ba899e54816a541e576c6f.png)](https://hackaday.com/wp-content/uploads/2018/10/hackaday-badge-expansion-header.jpg) 该徽章配有全键盘、液晶显示屏、音频扬声器和一个基本的编程环境，对于参加 Supercon 的好奇初学者来说，它将是一个友好的入口。对于我们的硬件黑客老手来说，有一个扩展板的标题:通向无限可能性的大门。串行通信是熟悉徽章扩展的良好起点，您应该带上自己的 USB 转串行适配器，以遵循我们的[徽章串行通信指南](https://hackaday.io/project/161859-2018-hackaday-superconference-badge/log/154556-serial-communications-with-badge)。

当您准备冒险超越通过串行链路与您的计算机交谈时，每个徽章还附带了这个扩展板。它插入徽章，引出所有用于通孔焊接的引脚，以及一些常见的表贴尺寸(0805、SO-8、SO-16、TSSOP-16、SOT-23)。最后但并非最不重要的，它有三个[低劣的附加头](https://hackaday.io/project/52950-shitty-add-ons)。我们的徽章[硬件黑客参考指南](https://hackaday.io/project/161859-2018-hackaday-superconference-badge/log/154554-hardware-hacking)将继续成长到(并通过)Supercon 来帮助回答你的问题。

[![](img/3a9e1690f7607662e6e5db5b0ff4084e.png)](https://hackaday.com/wp-content/uploads/2018/10/expansion-board.jpg)

扩展引脚可以通过 badge BASIC 进行控制。但是如果 BASIC 被证明是有局限性的，那么徽章也准备好了。徽章的核心是 Microchip 捐赠的 PIC32 系列处理器(以及闪存芯片)。扩展接头提供了使用 PIC 编程工具进行在线编程所需的所有引脚。微芯片的 PICkit (3 或 4)是受欢迎的选择，但还有其他选择。最后，安装了固件开发工具的计算机。我们的 [C 编程指南](https://hackaday.io/project/161859-2018-hackaday-superconference-badge/log/154555-guide-for-programming-in-c)列出了所需的下载和安装步骤。

上面的图像显示了一个红色的电路板，因为这是五个原型之一。我们使用 Macrofab 作为这个项目的合同制造商(他们慷慨地捐赠了一部分组装成本)，我们刚刚收到消息，500 个带有黑色阻焊膜的徽章的全面生产已经完成！

## 你要做什么？

为了适应复古计算的主题，默认固件中的大多数徽章功能(如 Z80 仿真)都是基于文本的。但是徽章屏幕并不局限于文字！我们很想看看它的图形功能能做些什么。甚至可能与扬声器播放的音乐同步？

[![](img/02e101f98cce122856ca5d4cba037239.png)](https://hackaday.com/wp-content/uploads/2018/10/2018-supercon-badge-expansion-board-595-shift-register.jpg)

[Simple circuit](https://hackaday.io/project/162054-shift-register-for-supercon-badge): 595 shift register and eight LEDs

另一个令人兴奋的前沿是多徽章黑客。通过串行将两个徽章相互连接起来是很简单的，所以只要你打开徽章，双人基本游戏就会被写入。但是这个想法还能走多远呢？串行引脚可用于桥接所有类型的[无线通信](https://hackaday.com/2018/10/19/which-wireless-is-right-wireless/)模块。或者，我们可能会看到有线徽章局域网的多徽章串行协议？

虽然我们已经为每个人设置好了串行端口，但通过一些额外的工作，PIC32 还可以通过 I2C 或 SPI 进行通信，从而打开了对大量电子外设的访问。有人会在 one-up 去年的相机徽章上附加相机模块吗？为 badge-brain 机器人添加电机/伺服控制器？唯一的限制是想象力、时间和一对 AA 电池的 3 伏电力。

## 做好准备，冒险在等着你

所以，带上你的 USB 串行适配器和你的 PICkit，加入我们的 Supercon 吧！徽章领取和工作区于周五(11 月 2 日)上午 9 点开放。虽然我们会提供一些组件，当然还有像烙铁这样的基本工具，但是会有很多人排队使用它们。最好带上你能随身携带的任何工具，以最好地帮助实现你的愿景。在周日晚上的闭幕式上，你被邀请向整个会议展示你所创造的一切。

留意[徽章项目页面](https://hackaday.io/project/161859-2018-hackaday-superconference-badge)上的参考资料更新，加入聊天室(有一个[一般用于 Supercon】，还有一个](https://hackaday.io/messages/room/273359)[专门用于徽章](https://hackaday.io/messages/room/276010))与志同道合的黑客联系。你们都有很棒的想法，让我们看看它们是如何实现的。这将是一次伟大的冒险！