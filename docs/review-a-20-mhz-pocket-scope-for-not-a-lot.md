# DSO 纳米 3 审查:一个 20 兆赫口袋'范围不是很多

> 原文：<https://hackaday.com/2018/08/06/review-a-20-mhz-pocket-scope-for-not-a-lot/>

示波器是任何电子工作台的基本工具，也是一种功能在过去几十年中成倍增长的仪器。几十年前完全模拟的 CRT 显示器现在已经被一种数字设备所取代，它具有昂贵的万用表、频率计数器等多种功能。在市场的顶端[当涉及到预算](https://hackaday.com/2015/02/10/the-one-million-dollar-scope-teardown/)时，天空是极限，低端延伸到基于商品微控制器的低带宽设备，价格接近零花钱。

这些超级便宜的示波器通常作为套件出售，尽管它们的带宽非常低，但由于编写良好的软件，它们是具有有用功能集的令人惊讶的功能强大的仪器。去年，我回顾了一款典型的型号，离开时感叹它缺少内部电池和质量不错的探头。如果有人能生产出一个便宜的微型望远镜，有合适的带宽，合适的探头和内置电池就好了！

碰巧的是，我没等多久就得到 DSO Nano 3 发布的消息，我的愿望得到了满足。让我们看看你能用不到 50 美元的便携式瞄准镜做些什么。

## 承诺

![The DSO Nano 3 being fed a 1MHz sine wave by our signal generator.](img/a37c7369bd5aebbd77949f4741f5f58a.png)

跑过 DSO Nano 3 立刻扬眉吐气。这是一个来自中国的小型袖珍望远镜，内置电池，合适的探头，最重要的是，声称有 20MHz 的带宽。最棒的是，它的售价只有区区 36 英镑(47 美元)！如果它符合带宽要求，它可能是一个真正的游戏改变者，所以我订购了一个来测试它。等了几个星期的国际包裹邮件，我把包裹放在我的长凳上。

令人惊讶的是，考虑到中国电子产品的趋势是用质量越来越高的盒子来包装，这种产品到达时没有包装，只有一个塑料密封袋。里面是一个说明书，一个迷你 USB 引线，一个示波器探头，一个 BNC 到 3.5 毫米插孔适配器，以及 DSO Nano 3 本身。我认为我打开了错误的包装，这是可以原谅的，因为最后一件东西看起来像第三代 iPod Nano。因此，范围的名称。我最大的猜测是，某个地方有一家生产假冒 iPods 的工厂，它们的外壳可以作为便携式示波器的便捷外壳。我无法想象它会让苹果的律师高兴，但无论如何，对于不是音乐播放器的东西来说，这都是一个有趣的选择，尽管我们在适当的时候会谈到这个问题。

在该装置的前面是相同的 2 英寸屏幕和滚轮控制，你会习惯从一个 iPod，这种相似性延伸到该装置的两侧和后部。值得一提的是，这个滚轮是一个带有点击动作的塑料滚轮，而不是苹果原装的滚轮。我不记得苹果音乐播放器有 USB 迷你插座来充电，但我知道 3.5 毫米耳机插座。在一边还有一个长方形的开口，我怀疑这可能是山寨 iPod 的音量轮，这里只是一个开口，通过它你可以看到 PCB。

[![Inside the DSO Nano 3, with most of the space given over to the battery.](img/8fba3805169df09a9250778194763067.png)](https://hackaday.com/wp-content/uploads/2018/07/dsonano3-internal.jpg)

Inside the DSO Nano 3, with most of the space given over to the battery.

## 里面是什么？

打开设备，显示器后面的大部分内部被锂聚合物电池占据，控制器后面的空间被电子设备占据。有一个[giga device gd32f 103](http://cn.gigadevice.com/product-series/26.html)ARM Cortex M3 处理器，一个 [Averlogic AL4228](http://www.averlogic.com/AL422B.asp) 384k 视频帧缓冲器，一个选择 [CPC1008N](http://www.ixysic.com/home/pdfs.nsf/www/CPC1008N.pdf/$file/CPC1008N.pdf) (PDF) MOS 开关，和一个 [AD9283-50](http://www.analog.com/en/products/analog-to-digital-converters/standard-adc/high-speed-ad-10msps/ad9283.html) 50 Msamples/S 模数转换器。

GD32F103 是该设备的大脑，AL4228 是一个用于保存采样波形的快速存储器，CPC1008Ns 在各种范围之间切换，AD9283 是模拟前端。这最后一部分有点意思，因为不像所有其他最近制造的产品，我们的产品有 1998 年的日期代码。一个 20 岁的芯片是如何进入 2018 年的设备的？它可能是老股票，但我大胆猜测，它来自我们都读过的巨大的中国电子元件回收市场。

值得注意的是，USB 端口的数据线连接到 GD32F103，尽管手册声称该插座除了充电没有其他功能，用 lsusb 快速查看显示没有设备出现。如果任何人有任何关于如何探查这个问题的提示或技巧，请在评论中告诉我们。

## 使用“范围

物理性质讲够了，操作起来是什么样的？一旦我按照建议用墙上电源插座的 USB 线而不是电脑 USB 插座给它充电，我就长按中心按钮给它通电。在闪屏之后，我得到了一个示波器显示的奖励。用提供的适配器将探头连接到 3.5 毫米插座，稍加操作，我就能够显示信号发生器的波形。

界面必须保持在苹果风格的点击轮的限制之内，这意味着选择不同的 rages 和探针是一个令人沮丧的过程，但一旦你习惯了，这是可能的。至于它的功能，它缺乏一些高级功能，你可能会期望一个更完善的范围，甚至是我在我审查的低带宽模型上发现的，这是一个非常基本的工具。

示波器应该提供两个基本功能:电压和时间周期的精确测量。我接着向 DSO Nano 3 提供了一系列测试波形，并将其与 RIGOL DS1054z 呈现的相同波形进行了比较。Nano 3 截图都是照片，如前所述，USB 端口纯粹是为了充电，并没有安装任何可以抓取图像的东西。

[![A 1kHz 3V pk-pk callibration signal, with the Nano 3 display inset top right over the Rigol display.](img/05c2f396d53220d8e495a78db194ccb6.png)](https://hackaday.com/wp-content/uploads/2018/07/dsonano3-1khz-square.jpg)

A 1kHz 3V pk-pk callibration signal, with the Nano 3 display inset top right over the Rigol display.

当天的第一个命令是将其连接到 Rigol 的校准终端(DSO Nano 3 没有自己的校准终端)。Rigol 提供了一个 3V 峰峰值 1kHz 方波，用于探头调整，与任何新探头一样，这个需要调整。在这种型号中，调节电容器在插头上，而不是在探头上，而且出乎意料地不需要太多注意。通过屏幕上的方波，我可以立即看到 Nano 3 的频率为 1kHz，但电压校准在 2.90V 时明显偏离 Rigol 的 3.01V。这将被证明是所有读数的一致问题，特别是正弦波的均方根值与更昂贵的仪器上测得的值相差很大。

[![A 20 MHz sine wave at 100mV pk-pk, as seen on a Nano3 screen.](img/edd9b38fb867b20eca373d28c92faf98.png)](https://hackaday.com/wp-content/uploads/2018/07/dsonano3-20mhz.jpg)

A 20 MHz sine wave at 100mV pk-pk, as seen on a Nano3 screen.

不过，这款仪器最重要的部分是 20 MHz 带宽。启动我古老的高级射频信号发生器，我开始通过 MHz 向它输入信号，看看它的表现如何。使用 Rigol 作为监控器，将所有电压调节至 100mV RMS，馈电通过 50 ohm 端接同轴电缆进行，如靠近页面顶部的图片所示。

令人失望的是，当输入 20MHz 正弦波时，Nano 3 几乎无法解决这个问题。产生了参差不齐的显示，幅度很低，频率测量值变化很大。左边的照片显示读数为 22.2 MHz，它摆动到 18 MHz，试图了解该频率下的输入。

[![A 10 MHz 100mV pk-pk sine wave as seen through the Nano 3.](img/eff2a45adba74690380c37ce8ecbe804.png)](https://hackaday.com/wp-content/uploads/2018/07/dsonano3-10mhz.jpg)

A 10 MHz 100mV pk-pk sine wave as seen through the Nano 3.

在 10 MHz 时，图像变得稍微好一点。电压仍然很低，但接近正弦波的东西出现在屏幕上，它正确地解析了频率。所有这些读数都是在仪器设置在 1X 范围内时获得的，因为输入来自 50 欧姆端接线路，并且没有衰减器。

当频率降至 10 MHz 以下时，该仪器开始变得更加有用。我们的峰峰值电压更接近 Rigol 设置的 100mV，波形看起来也是如此。电压校准仍有一些差异，但这已经成为一个更可信的设备。

## 复杂的裁决

[![A 1MHz 100mV pk-pk sine wave as seen on the Nano 3.](img/2c3ada68cbeebdeb2ecf613fbf7f81d6.png)](https://hackaday.com/wp-content/uploads/2018/07/dsonano3-1mhz.jpg)

A 1MHz 100mV pk-pk sine wave as seen on the Nano 3.

那么在使用了一段时间 Nano 3 之后，我对它有什么看法呢？答案是极其复杂的，一方面，这是一个惊人的设备，可以真正重新定义廉价的地下室口袋的范围提供了什么，但另一方面，它设法错过了它的怪癖和缺点轻微的目标。任何这样的“可以脱离其他袖珍示波器的数百 kHz 带宽的示波器”都值得一看，但它过于乐观的带宽要求和一致的电压校准使它不是一个容易的购买决定，如果它相当复杂的接口还不够的话。

iPod 外壳是一个不错的想法，但似乎示波器要适合它就必须做出太多的妥协。如果将迷你 USB 端口替换为微型 USB 端口，将 3.5 毫米插座替换为 BNC，将点拨轮控件替换为更有用的东西，并应用某种电压校准曲线，我可以忘记 20MHz 带宽的说法，并将它视为一个相当漂亮的 10MHz 袖珍示波器。但事实上，我只能向你推荐这个，如果你真的**必须**有办法看到一个 10 MHz 的波形，可以在一个微小的空间不惜一切代价。我建议新手购买低带宽的示波器，但我不能对这个型号提出同样的建议。

也许最好把这个设备看作是第一次尝试，预示着更好的未来。即使有了这种硬件，也肯定有办法在软件中解决它的一些缺点，所以当不可避免的抄袭工具和后续版本出现时，也许它们会有用得多。我希望如此，没有什么比拿出一个看起来像 iPod 的东西并在上面检查波形更能说明极客时尚了！