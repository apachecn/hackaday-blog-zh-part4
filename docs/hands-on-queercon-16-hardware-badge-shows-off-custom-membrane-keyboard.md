# 动手操作:Queercon 16 硬件徽章展示定制薄膜键盘

> 原文：<https://hackaday.com/2019/08/16/hands-on-queercon-16-hardware-badge-shows-off-custom-membrane-keyboard/>

年复一年，奎尔康徽章始终令人印象深刻。我认为这些徽章最令人印象深刻的是，它们似乎抛弃了前一年的所有设计想法，重新开始，但每次都设法发现独特和令人上瘾的审美。

今年有两个硬件徽章是由[埃文·麦凯](https://twitter.com/AKIOOHTORI)、[乔治·卢森](https://twitter.com/duplico)、[塔拉·斯卡伯](https://twitter.com/Skittishandbus)和[托托格](https://twitter.com/sidechannel_org)组成的团队制作的。这里显示的是昵称为“Q”的徽章，因为它与字母相似。两者都让你进入会议，两者都是电子互动的，但这一个就像一个替代现实游戏(ARG)的控制面板，鼓励互动和有意义的对话。另一个徽章是“C”徽章。它更被动，但却是 ARG 中的一个关键——你不能只与一种徽章互动，你必须与两种徽章类型的人合作，这样没有购买 Q 徽章的 Queercon 参与者仍然可以享受乐趣。

这个徽章上最引人注目的功能是一个定制的薄膜键盘，专为在会议上玩所有徽章的互动游戏而定制。但我发现 eInk 屏幕、用于连接的 RJ12 插孔、LED 和挡板的排列组合在一起，实现了功能和艺术的完美平衡。休息后，请加入我的行列，近距离了解这款硬件的特别之处。

## 有多少徽章有自定义键盘？

 [![Queercon16-2019-q-badge-front](img/b9f81dc12fbd4c8d0477f1ffb39586bb.png "Queercon16-2019-q-badge-front")](https://hackaday.com/2019/08/16/hands-on-queercon-16-hardware-badge-shows-off-custom-membrane-keyboard/queercon16-2019-q-badge-front/)  [![Queercon16-2019-q-badge-rear](img/dabcb19cf985a2553b4785730019cfeb.png "Queercon16-2019-q-badge-rear")](https://hackaday.com/2019/08/16/hands-on-queercon-16-hardware-badge-shows-off-custom-membrane-keyboard/queercon16-2019-q-badge-rear/) 

乍一看，很容易忽略这个键盘的特别之处。它占据了徽章表面的圆形区域，有三样东西吸引了我的眼球，挑战了我对这些薄膜键盘的看法。首先，全彩印刷和表面处理都做得非常好。第二，这不是一个无聊的按键布局(好吧，方向键有点无聊)，而是一个定制的参数。最后，这个键盘后面还有 led 灯！

 [![Keyboard surface finish](img/31133baf7d006a1a5abdc2a6ec2c35ce.png "Queercon16-2019-membrane-keyboard-front")](https://hackaday.com/2019/08/16/hands-on-queercon-16-hardware-badge-shows-off-custom-membrane-keyboard/queercon16-2019-membrane-keyboard-front/) Keyboard surface finish [![Keyboard stack up](img/7c623128f549c2dcc2c237be22e34513.png "Queercon16-2019-membrane-keyboard")](https://hackaday.com/2019/08/16/hands-on-queercon-16-hardware-badge-shows-off-custom-membrane-keyboard/queercon16-2019-membrane-keyboard/) Keyboard stack up [![LEDs shine through the windows in the keyboard](img/c5ae86f12bfc65200a359dfadb96a548.png "Queercon16-2019-LEDs-integrated-in-keyboard")](https://hackaday.com/2019/08/16/hands-on-queercon-16-hardware-badge-shows-off-custom-membrane-keyboard/queercon16-2019-leds-integrated-in-keyboard/) LEDs shine through the windows in the keyboard

Evan MacKay 说，当他发现薄膜键盘可以用 CMYK 全色打印时，他对使用薄膜键盘的想法产生了兴趣。这个过程实际上相当简单，只需要一张机械图纸和印刷过程的美术，两者都以 PDF 文件的形式发送。制造商向他们提供了用于在薄膜下集成 led 的垫片样品，这些垫片的厚度有 5、7 或 10 密耳。看键盘的下面，你可以看到 LED 和按钮圆顶的空间。叠层交付时已经安装了粘合层。只需剥去背衬，贴在你的 PCB 上。

这些按键压印在薄膜上，这意味着没有单独的机制将它们弹回。这偶尔会导致卡住的按钮出现故障，但通常按钮会再次弹出。下一步应该是包括按压后会弹回的金属圆顶，但这当然会增加成本。

 [![Queercon16-2019-stunning-epaper-display](img/949776cf0d26a1ac67df44638b2b9251.png "Queercon16-2019-stunning-epaper-display")](https://hackaday.com/2019/08/16/hands-on-queercon-16-hardware-badge-shows-off-custom-membrane-keyboard/queercon16-2019-stunning-epaper-display/)  [![Queercon16-2019-rear-silk-and-LEDs](img/a2fcf4422bf221d6c2d15c4ccd163c91.png "Queercon16-2019-rear-silk-and-LEDs")](https://hackaday.com/2019/08/16/hands-on-queercon-16-hardware-badge-shows-off-custom-membrane-keyboard/queercon16-2019-rear-silk-and-leds/)  [![Queercon16-2019-LED-bezels](img/ab2ef131fe9c47e813da3a0ca112a639.png "Queercon16-2019-LED-bezels")](https://hackaday.com/2019/08/16/hands-on-queercon-16-hardware-badge-shows-off-custom-membrane-keyboard/queercon16-2019-led-bezels/) 

令人惊叹的 2.9 英寸 128×296 eInk 显示器为显示您的姓名和玩 ARG 提供了一个高分辨率的游戏场所。它比去年的徽章中使用的字符 LCD 屏幕提供了更多的多功能性(但我必须说我也喜欢这个想法！).

在屏幕的两个长边上，你会发现六个侧视图 RGB LEDs。最初，这些并不意味着有挡板，但早期的测试证明，太多的光漏在零件的顶部，所以黑色的 3D 打印支架被添加。PCB 的外边缘有 12 个全彩色 led，6 个在顶部(俯视型)，6 个在底部(侧视型)。

这些徽章由 TI CC2640R2 驱动，它具有 ARM Cortex-M3 内核，并将蓝牙带到派对中。LEDS 的控制由 Holtek HT16D35B LED 控制器提供，该控制器是一个 28×8 恒流驱动器。一对 AA 电池使用 Evan 最喜欢的 Skyworks 稳压器为徽章供电，即使电池电压降至 1.2 V，徽章也能保持运行——我认为这是 AAT1217。

## C 徽章和参数

 [![Queercon16-2019-c-badge-populated](img/60b7125f01dd91155078cfd4059530d3.png "Queercon16-2019-c-badge-populated")](https://hackaday.com/2019/08/16/hands-on-queercon-16-hardware-badge-shows-off-custom-membrane-keyboard/queercon16-2019-c-badge-populated/)  [![Queercon16-2019-c-badge-crew](img/aca990d67eb8223dbafc25d4f3ce14c2.png "Queercon16-2019-c-badge-crew")](https://hackaday.com/2019/08/16/hands-on-queercon-16-hardware-badge-shows-off-custom-membrane-keyboard/queercon16-2019-c-badge-crew/)  [![Queercon16-2019-c-badge-crew-rear](img/5cd32c5254f9f0f5c85b9f65eb1493b2.png "Queercon16-2019-c-badge-crew-rear")](https://hackaday.com/2019/08/16/hands-on-queercon-16-hardware-badge-shows-off-custom-membrane-keyboard/queercon16-2019-c-badge-crew-rear/) 

这是 C 徽章，适用于所有选择不购买 Q 徽章的 Queercon 与会者。图中的乘务人员徽章是空的，但在 attendee 版本中，您可以看到一个看起来像以太网或电话的插孔。两者都不是，我被背面的丝网印刷逗乐了，上面写着“不要插入电话杰克·PLZ！”。这是一个 RJ12 6P6C 连接器，可与每个 Q 徽章提供的电缆配合使用。这是徽章之间的连接方法，以进一步 ARG。

追求互动游戏的人必须找到 Q 徽章和 C 徽章的持有者来交换数字代币。Q 徽章持有锁、硬币和相机，而 C 徽章持有钥匙、鸡尾酒和旗帜。随着游戏的进行，任务可以从操作者(员工徽章)处下载。在休息室内甚至有一个基站可以报告你的进度。每当有人检查这些支柱中的一个，他们的总体进展就会被添加到总和中，并且支柱开始改变颜色——这是公共利益的记分牌。

![](img/7bceba7f087c581dde15f878812a4a80.png)

Queercon 16 徽章的整体展示堪称全垒打。Tara Scape 负责今年会议的艺术设计，并将其融入到徽章中，从 PCB 艺术到薄膜键盘，甚至是盒子的内部。这是一个完整的包裹，感觉就像你得到了一份礼物，每个人都会珍惜这个帮助他们在会议上体验的彩色小宝石。

Evan 已经在徽章团队工作了七年，我问他是否为此付出了代价。他给了我一个强调，不。看来他有足够的精力进行下一个大的建设。我无法想象如何超越这个小规模硬件做得很好的例子，但我相信他们会以某种方式实现它。从我见过的第一个 QC 徽章([软盘](https://hackaday.com/2014/09/15/the-queercon-11-badge/))到乌贼的[俯冲线](https://hackaday.com/2016/08/10/what-we-learned-from-the-2016-queercon-badge/)、QC14 的[辉煌立方体](https://hackaday.com/2017/08/07/inside-this-years-queercon-badge/)、对旧库存展示的巧妙利用，以及今年的“彩虹银翼杀手”主题，这个徽章团队的背面目录是一本灵感的镀金大部头。