# 佩戴式内窥镜让你的手指进行探测

> 原文：<https://hackaday.com/2021/09/03/wearable-scope-lets-your-fingers-do-the-probing/>

对于分秒必争的疯狂黑客会议，这款由[aniketdhole] 制造的带有指尖探头的[前臂安装示波器可能正是您所需要的。嗯，也许吧。目前还不清楚*为什么*你可能想在手臂上戴一个示波器，把手指伸进通电的电子设备听起来特别像你母亲可能告诉你不要做的事情，但不管怎样，它还是出现了。](https://hackaday.io/project/180350-oscilloscope-band)

[![](img/c5d939e66bc7aebed8e2252afd2cc3e7.png)](https://hackaday.com/wp-content/uploads/2021/08/armscope_detail.jpg) 示波器由一个 3D 印刷安装的 nRF5340 评估板组成，顶部有一个 SPI 连接的 Adafruit 2.8”TFT 显示器。通过从电路板的 ADC 和接地引脚引出的一对导线，[aniketdhole]只需要一点代码就可以将它们粘合在一起，并在显示器上显示一些基本的信号可视化效果。它已经针对 Arduino 和一些电位计控制的电压产生的 PWM 信号进行了测试，但在当前配置下，任何比这更疯狂的要求可能都有点过分。

在未来，[aniketdhole]希望增加一些降压电路，以便您可以探测比 nRF5340 正常处理更高的电压，以及允许电流测量的分流器。一旦硬件到位，下一步的工作将是改进可触摸的用户界面，让用户调整设置和在功能之间切换。

即使你不喜欢安装在手臂上的示波器，这仍然是一个有趣的可穿戴实验平台。把足够多的传感器扔进去，我们确信有很多黑客不介意绑上这些传感器。

The [HackadayPrize2021](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)