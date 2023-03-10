# 拆卸:AppLights 个性化投影

> 原文：<https://hackaday.com/2019/02/27/teardown-applights-personalized-projection/>

听着，听起来很伤人，但总得有人说出来。结束了，好吗？你必须承认并继续前进。当然，你可以在一月的一两个星期里安然无恙，但是现在事情变得越来越奇怪了。无论你如何努力抗争，事实就是事实:假期结束了。是时候在邻居们真正开始谈论之前收拾好所有的灯和装饰品了。

[![](img/7c7ee756c8c4507141a7f11c09b47cab.png)](https://hackaday.com/wp-content/uploads/2019/02/projector_official.jpg)

Fun Fact: It can’t actually do this

但是不要担心，因为有好的一面。零售商正在为他们的下一个销售旺季做准备，这意味着现在世界各地的清仓货架可能会成为节日灯饰和装饰的大本营。几年前，这对于普通的黑客或制造者来说不会很有趣，毕竟，你只能用一串闪烁的灯做这么多事情。但是今天，节日装饰品充满了你所期待的高科技特色，这些特色来自于那些打算在未来十个月左右被淘汰的小玩意。

举个例子，几周前我在家得宝的清仓区发现的“AppLights Personalized Projection”。该设备宣传能够在您的墙上投影多色自定义消息和动画，并通过蓝牙与您的 Android 或 iOS 设备上的配套应用程序进行配置。至少我们可以假设该设备必须包含一个相当强大的 RGB LED，一个 LCD 来照亮，以及某种蓝牙兼容的微控制器。为了 20 美元，我认为值得一试。

大约在去年的这个时候，经常阅读 Hackaday 的读者可能还记得我为一台圣诞激光投影仪做了一次拆卸。在里面，我们发现了功率相当大的红色、绿色和蓝色激光器，以及让它们运转的所有光学器件和支持硬件。这是一个名副其实的激光游乐场，售价 14 美元。让我们看看 AppLights 投影仪是否是一个类似的电子聚宝盆，以及我们是否有一个新的 Hackaday 假日传统。

## 保持简单

卸下投影仪底部的螺钉后，外壳的上半部分很容易脱落，露出内部。正如预测的那样，该设备包含一个 LED，一些光学器件和一个小型液晶显示器，供光线通过。看起来机箱内确实有很多浪费的空间，但总的来说，内部结构正是您所期望的，因为我们看到的基本上是以最低价格制造的 LCD 投影仪。

[![](img/ed7f4021702a4ed8bdc2ae7b5e35b137.png)](https://hackaday.com/wp-content/uploads/2019/02/projector_internal.jpg)

这里有一个有趣的注意事项是，外壳有一个密封关闭的电池舱。似乎在某个时候，设计者想到了允许用户使用标准 AA 电池来运行投影仪，但是由于运行时间非常短，这个功能很可能被删除了。尽管人们确实想知道电池供电的假日投影仪会有什么优势，因为它根本不需要移动。

## 热量管理不当

尽管布局如此简单，AppLights 投影仪的设计并非没有缺陷。正如你可能在前面的图片中注意到的，设备的冷却系统似乎是一个非常糟糕的设计。显然，从 60 毫米风扇吹到电源周围的少量空气是冷却 LED 的全部。更糟糕的是，看起来像是风扇“格栅”的东西实际上是实心的。除了两个小孔，没有让冷空气进入设备的入口。

 [![Note the fan wires pinched during assembly.](img/125c830a01e671a619dbca56736fedc6.png "projector_thermal1")](https://hackaday.com/2019/02/27/teardown-applights-personalized-projection/projector_thermal1/) Note the fan wires pinched during assembly. [![projector_thermal2](img/3161c9026a2a41c8499ced4ccea5c945.png "projector_thermal2")](https://hackaday.com/2019/02/27/teardown-applights-personalized-projection/projector_thermal2/) 

虽然你可能会认为这款设备预期的工作环境温度意味着可能不需要强大的冷却系统，但很难想象这种安排会有什么作用。如果这个设备出现故障，几乎可以肯定是由于烹饪本身。

## 异常强大的电源

当深入挖掘投影仪时，我惊讶地发现，夹在冷却风扇和 LED 散热器之间的小电源似乎……*而不是*可怕。它是一个独立的可移动模块，配有自己的塑料外壳，看起来构造合理，交流侧有一个保险丝，并且[不像我们解剖的其他廉价设备中的电源](https://hackaday.com/2018/04/23/teardown-led-bulb-yields-tiny-ups/)，它实际上是电源隔离的。它甚至包括前面提到的风扇。

 [![projector_psu](img/719036b949cd240585caf07ba6323ac2.png "projector_psu")](https://hackaday.com/2019/02/27/teardown-applights-personalized-projection/projector_psu/)  [![projector_psu_test](img/f91543550996fa6f1c456378d0073eb1.png "projector_psu_test")](https://hackaday.com/2019/02/27/teardown-applights-personalized-projection/projector_psu_test/) 

当连接到可调负载时，我们看到电源能够在 18 VDC 下提供 1.35 A 的电流，然后电压开始波动，风扇减速。交流侧已经为您预先布线，当与我们之前介绍过的一个流行的 DPS 模块配对时，这个小模块可以成为轻型工作台电源[的良好基础。](https://hackaday.com/2018/03/19/diy-power-supply-and-ts100-outlet-combo-shows-off-great-layout/)

## 让那里有光

在我打开 AppLights 投影仪之前，LED 本身可能是我认为该产品最有趣和最有可能重复使用的部分。即使投影仪中没有其他值得保留的东西，一个高输出 RGB LED 和相关的镜头对各种照明项目都是有用的。我很高兴地告诉大家，这一部分已经成熟，可以收获了。

 [![projector_led1](img/09c1e891f544d4474b289072cd9d227f.png "projector_led1")](https://hackaday.com/2019/02/27/teardown-applights-personalized-projection/projector_led1/)  [![projector_led2](img/401e1c32660620e0500309720e5724be.png "projector_led2")](https://hackaday.com/2019/02/27/teardown-applights-personalized-projection/projector_led2-2/) 

20×20 mm 模块的后部标有“LY18423”，尽管在搜索时似乎没有返回任何有用的信息。但在浏览全球速卖通和比较图像后，我相当有信心这是一个 10W 模块。它用一些非常漂亮的彩色编码硅线连接，末端有热收缩管，甚至在它和散热器之间有适当的热化合物。至少，设备的这一部分做得比较好。

## 行动的智囊

AppLights 投影仪的所有电子设备都位于一个 PCB 上，该 PCB 逻辑上分为包含三个 LED 驱动器、LCD 控制器和蓝牙模块的部分。不幸的是，LCD 控制器被一种邪恶的黑色环氧树脂覆盖，所以这些组件是一个谜。有趣的是，在 PCB 的顶部中心，我们可以看到标有“- BAT +”的焊盘；证实了这个装置曾经需要电池供电的理论。

 [![Must have been a sale on larger ZIF connectors.](img/e3cfa3ed3fce76f3699dc65365d15eec.png "projector_pcb1")](https://hackaday.com/2019/02/27/teardown-applights-personalized-projection/projector_pcb1/) Must have been a sale on larger ZIF connectors. [![projector_pcb2](img/2fe3934736db1016b5806dd2a70189af.png "projector_pcb2")](https://hackaday.com/2019/02/27/teardown-applights-personalized-projection/projector_pcb2/)  [![The traces can easily be matched with the datasheet.](img/f0b74cf5fcfd12651c114dfbbc20941a.png "projector_pcb3")](https://hackaday.com/2019/02/27/teardown-applights-personalized-projection/projector_pcb3/) The traces can easily be matched with the datasheet.

令人耳目一新的是，不仅蓝牙模块上的标记没有被模糊，而且搜索数字[实际上导致通过 FCC ID 数据库](https://fccid.io/2AH7AKW2541A/User-Manual/user-manual-2993004)找到数据表。有了引脚排列，我们可以从轨迹中看到，TTC2541 模块似乎正在与 I2C 上空的黑色斑点通信。通过连接逻辑分析仪并在智能手机应用程序中选择不同的选项，这一事实得到了证实。

[![](img/ade5a69aeeeed26d5c7467122dbaffcf.png)](https://hackaday.com/wp-content/uploads/2019/02/projector_i2c_capture.png)

## 进一步黑客攻击

最初我希望这次拆卸会以 AppLights 投影仪发出我们心爱的扳手的图像结束，但在使用逻辑分析仪进行检查时，似乎智能手机应用程序中提供的图像和动画集合被刻录到 LCD 控制器中，蓝牙模块只是传递用户想要显示的 ID。让投影仪显示除了已有的内容之外的任何内容，可能意味着手动接管 LCD 的控制权。

这很容易，但在这一点上，我可能应该提到投影机的分辨率是糟糕的。LCD 面板只有 32×24，每个“像素”是一个直径大约为 0.5 毫米的点。实际上，这意味着投影仪一次只能显示三个文本字符。任何比这更长的，它会在屏幕上滚动它们。(滚动速度至少可以在软件中设置。)我肯定有才华的像素艺术家可以用 32×24 的胖点做出很酷的东西，但我肯定不是其中之一。

## 淘气还是乖？

这些拆卸本身并不意味着对产品的审查。话虽如此，我确实玩了“AppLights 个性化投影”足够自信地说，作为一个产品，它相当差。智能手机应用程序(顺便提一句，这是必需的)一团糟，基本的图像很模糊，只能投射很短的距离。如果你对它作为真正的节日装饰感兴趣，我当然不会推荐它。

但就硬件而言，它包含一个非常好的交流/DC 电源，一个可以轻松移植到不同项目的大功率 LED，甚至还有一个相当完善的 TTC2541 BLE 模块。液晶显示器和它的环氧树脂斑点控制器有点令人失望，但鉴于低分辨率，我不知道它到底能用来做什么。

总的来说，我想说这是勤劳的黑客可以在清仓架上以低廉的价格找到有用硬件的又一个好例子。当然，你可以以低于投影仪清仓价的价格购买单个组件，但你仍然需要等待数周才能将它们运送给你。但更重要的是，拆开这些东西来发现新的组件是乐趣的一半。就当是迟到的圣诞礼物吧。