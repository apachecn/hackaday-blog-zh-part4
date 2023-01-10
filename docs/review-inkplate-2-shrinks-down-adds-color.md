# 评论:Inkplate 2 缩小，增加颜色

> 原文：<https://hackaday.com/2022/12/07/review-inkplate-2-shrinks-down-adds-color/>

普通黑客读者可能会想起 Inkplate 系列设备:开源一体化开发板，将 ESP32 的功能和多功能性与从商业电子阅读器中回收的电子纸显示器相结合。Inkplate 采用了面向亚马逊 Kindle 等读者的锐利、高速显示器，并将它与让它工作所需的所有硬件和软件捆绑在一起，为任何希望认真对待电子纸的人提供了一个交钥匙平台。

鉴于他们的屏幕是从回收的阅读器中取出的，所以之前的 Inkplate 条目出现在熟悉的 6 英寸和 10 英寸版本中就不足为奇了。甚至还有一款升级的 6 英寸机型，它受益于更新的阅读器技术，采用了触摸感应背光面板，[我们去年仔细观察过它](https://hackaday.com/2021/06/21/review-inkplate-6plus/)。它们的大显示屏非常适合壁挂式应用，例如家庭通知中心或不断变化的艺术展示。此外，正如你所料，Inkplate 是任何希望推出自己的定制电子阅读器的人的[理想选择。](https://hackaday.com/2021/08/20/inkplate-comes-full-circle-becomes-true-open-reader/)

[![](img/df827caa7fffb3d06f3cfc3f06d26925.png)](https://hackaday.com/wp-content/uploads/2022/12/soldered_logo.png) 但是当然，并不是每个应用都需要这么大的屏幕空间。事实上，对于某些任务，如此大的显示器可能会被认为是一种负担。看到他们现有的产品阵容中的空白，焊接电子公司(以前的 e-radionica)的人最近推出了小型 Inkplate 2。这种新的微型 Inkplate 使用与其更大的前辈相同的软件库，但由于其 2.13 英寸的三色显示器，使其适合更广泛的潜在项目。此外，它比更大的墨水瓶便宜得多，仅售 35 美元。

考虑到为 Inkplate 2 发起的众筹活动在短短 72 小时内就超过了目标，显然人们对这款新的较小型号很感兴趣。但如果你仍然不确定这是否是你一直在等待的电子纸解决方案，也许我们可以提供帮助 Soldered 的人送来了 Inkplate 2 的预生产版本供我们试用，所以让我们试驾一下，看看有什么大惊小怪的。

## 一台精干、吝啬的 E-Ink 机器

由于屏幕更大，早期的 Inkplate 型号在 PCB 上有足够的空闲空间来放置额外的硬件，如实时时钟、温度传感器和 MCP23017 I/O 扩展芯片。但 Soldered 不得不放弃 Inkplate 2 上的这种奢侈品，因为较小的 PCB 已经与 ESP32 WROVER-E、CH340C UART 芯片、MCP73831 充电控制器以及让每个人满意所需的各种无源器件紧密包装在一起。

[![](img/b1b7e35b0635c76ed571a0d1d1caed03.png)](https://hackaday.com/wp-content/uploads/2022/12/inkplate2_front.jpg)

但是，即使没有以前型号的 IO 扩展硬件，Inkplate 2 仍然有相当数量的 GPIO 引脚可用，这些引脚沿着电路板的顶部分布，背面还有一个 Qwiic 兼容的 easyC 连接器。你可以通过 I2C 连接外部传感器，当然，如果你真的需要更多的引脚，添加自己的 I/O 扩展芯片也是一个选择。

也就是说，我确实怀念以前的 Inkplate 模型提供的交互性。6 英寸和 10 英寸的 PCB 前面有触摸感应垫，6PLUS 有完整的触摸屏。虽然电路板确实很紧，但我仍然认为他们可以在侧面安装一个 SMD 瞬时按钮。按照现在的情况，如果你需要一种与你正在运行的程序交互的方式，你需要通过连接你自己的按钮来占用一个 GPIO 管脚。

[![](img/52a5db0fc135b2302869541ca9751add.png)](https://hackaday.com/wp-content/uploads/2022/12/inkplate2_back.jpg)

PCB 空间有限的另一个原因是 ESP32 的板载天线，最佳做法是将其悬挂在 PCB 边缘，或在其后面留出一个缺口。不幸的是，这两个选项在这种情况下都不起作用，这意味着 MCU 的无线电接收可能会减少。对于许多应用来说，这可能是也可能不是什么大不了的事情，但即便如此，Soldered 还是在 Inkplate 2 上增加了一个外部天线。虽然图中的原型只是焊接了一点电线，但最终的生产硬件在板上有一个合适的 IPX 连接器。

## 颜色，有成本

由于没有任何旧的两英寸电子阅读器来挽救显示器，锡焊不能吹嘘他们这次出售的每台设备都使硬件免于被填埋。但是，尽管墨盘 2 中使用的新制造的电子纸可能不如墨盘 6 和墨盘 10 中使用的电子纸那么绿，但它能够呈现非常漂亮的红色。

[![](img/b24e913b4f707f75a0d19002f7b8896a.png)](https://hackaday.com/wp-content/uploads/2022/12/inkplate2_sunlight.gif)2.13 寸面板的分辨率为 212 x 104，PPI 为 111。结合宽广的视角和极好的日光可读性，它本人看起来很棒。在 B & W 模式下，刷新率相当不错，但应该注意的是，使用第三种颜色会*显著*延迟该过程——在显示三色图像后，预计需要等待 20 到 30 秒，屏幕才会完全稳定下来。

但是在实践中，这并不是什么大问题。正如 Soldered 在活动页面上的演示中所展示的，并且当您亲自玩硬件时会很快了解到，Inkplate 2 最适合作为显示缓慢变化的数据的辅助显示器。把当天的天气预报或者你接下来几个小时的日程安排放在上面。只要您不要求信息每 15 分钟左右更新一次，它可能非常适合 Inkplate 2。

## 墨水瓶体验

虽然硬件足够坚固，但展会的真正明星是非凡的软件、文档和体验，它们是设备 Inkplate 系列的一部分。对于高端型号来说，Inkplate 10 的价格高达 169 美元，这种支持水平是理所当然的。毕竟，如果你支付高价，你会期待优质的体验。但是，Inkplate 2 美元的标价让你可以进入这个完整的生态系统，这是一个令人惊喜的事实，也许是该产品最令人兴奋的事情之一。

与以前的型号一样，Inkplate 2 可以使用 Arduino IDE 或 MicroPython 进行编程，并且还具有独特的“外设模式”,可以通过 UART 发送的命令直接控制该设备。Soldered 还为[提供了一个在线图像转换器](https://inkplate.io/home/image-converter/)(已经为三色显示器进行了更新)[以及一个 GUI 生成器](https://inkplate.io/home/gui-editor/)，尽管鉴于 Inkplate 2 缺乏触摸屏，尚不清楚后者是否会为其更新。

[![](img/52e9c4917baafac004a630480d31f9cd.png)](https://hackaday.com/wp-content/uploads/2022/12/inkplate2_arduino.png)

启动并运行 Inkplate 2 非常简单。将电路板定义和库添加到 Arduino IDE 并编辑 HTTP 示例以指向我的服务器只花了几分钟。从那里开始，这个设备会定期用我提供给它的任何图像更新它的显示。结合电脑端的一些 Python 语言，这就形成了一个快速的桌面显示，[将显示我扔给它的任何东西](https://hackaday.com/2020/03/26/stay-informed-how-to-pull-your-own-covid-19-data/)。

## 物有所值

[![](img/fff31b59b26e80e7ffe93255166e4b28.png)](https://hackaday.com/wp-content/uploads/2022/12/inkplate2_case.jpg) 现在让我们回到现实中来。如果你正在阅读 Hackaday，你完全有能力在没有人握着你的手的情况下将一台 ESP32 连接到一个小型电子纸显示器上。你可能也知道，易贝的这两个设备的现行价格低于 35 美元的焊接价格。当然，它们不会在一个方便的小 PCB 上，你也不会得到 USB-C 的[统一能力，但这些很难阻止展示。](https://hackaday.com/2022/12/06/usb-c-introduction-for-hackers/)

尽管如此，我仍然认为 Inkplate 2 提供的文档、工具、库和最终用户体验比这个统一解决方案的额外成本更值得。这可以说是在小型电子纸显示器上获取信息的最直接、最轻松的方式，可以让你腾出手来处理更重要(老实说，也更有趣)的任务，比如弄清楚如何生成你想要推送给它的数据。