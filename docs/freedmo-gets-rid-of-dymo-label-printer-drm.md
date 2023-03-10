# #FreeDMO 摆脱 DYMO 标签打印机数字版权管理

> 原文：<https://hackaday.com/2022/03/30/freedmo-gets-rid-of-dymo-label-printer-drm/>

DYMO 550 系列打印机营销简介称“DYMO LabelWriter 550 Turbo 标签打印机配有独特的自动标签识别功能”，从 marketing-ese 翻译过来，意思是“这台打印机的 goshdarn 热敏标签中有 DRM”。是的，DRM 在你通常购买的普通卷纸的标签上。[FREEPDK]也不喜欢这样，并记录了一个#FreeDMO 设备,以摆脱另一个消费者自由限制，真正的黑客方式。

你只需要普通的 BluePill 板和两个电阻，几根额外的电缆使安装变得干净和可逆——如果你需要，你肯定可以焊接到 DYMO 打印机的 PCB 上。本质上，你拦截 RFID 阅读器连接，其中 BluePill 同时充当 I2C 外设和控制器，转发来自 RFID 阅读器的数据并修改它——但它也可以完全模拟预先确定的标签并跳过阅读器。如果你可以从这个项目的发现中受益，你也应该花一点时间，在你的 Android NFC 手机的帮助下，[在一个单独的存储库中共享你的墨盒数据](https://github.com/free-dmo/free-dmo-tag-dump),让我们所有人更容易阻止未来的 DRM 改进。

布线说明非常清楚，容易遵循，只要你得到的电缆具有相同的颜色引出线，但用针重新布线不会伤害任何人。从那里，只需完成一些常见的步骤，将固件刷新到 BluePill 板中，如果您想使布线更简单或硬编码现有类型的标签，请重新编译代码。这样，你得到了标签计数器倒带和欺骗，绕过了限制，不应该有摆在首位。

我们获得的设备的真正所有权是最重要的，它帮助我们摆脱限制和约束，这些限制和约束使我们的生活变得更糟，因为它们成为一种趋势，我们旅程中的这一步与绕过 Keurig coffee pod 重复使用限制的方式没有太大区别。如果每次[有人试图像梁永能一样将 DRM 添加到 3D 打印机灯丝](https://hackaday.com/2014/04/10/resetting-drm-on-3d-printer-filament/)中时我们都有一枚镍币，我们会有两枚镍币——这不是很多，但奇怪的是[它发生了两次](https://hackaday.com/2016/01/12/hacking-chipped-3d-printer-filament-on-the-da-vinci-printer/)。EFF 在上个月报道了梁永能 DRM [，一个月后，我们很高兴看到它被破解。](https://www.eff.org/deeplinks/2022/02/worst-timeline-printer-company-putting-drm-paper-now)

想知道为什么这甚至是一个问题？这是一个复杂的问题，这一段有太多要谈的，但我们[已经谈了我们的理由，并给你举了一些例子](https://hackaday.com/2022/01/08/the-year-of-owning-it/)，因为我们[继续用我们的工具辅助抗议来对抗这些趋势](https://hackaday.com/2022/01/15/hacking-is-hacking/)。当[苹果](https://hackaday.com/2010/02/13/ipod-shuffle-headphone-remote-reverse-engineered/)、[联想](https://hackaday.com/2016/02/11/unlocking-thinkpad-batteries/)、[小米](https://hackaday.com/2019/10/24/reverse-engineering-xiaomi-iot-firmware/)、[蓝光](https://hackaday.com/2014/09/08/unbricking-a-bluray-drive/)、[任天堂](https://hackaday.com/2021/06/13/super-mario-bros-35-lives-again-with-a-fan-made-server/)和其他人试图阻止我们的时候，我们发明了新的方法和工具来达到目的。