# 简单的探头探测出电磁干扰

> 原文：<https://hackaday.com/2021/05/21/simple-probe-sniffs-out-emi/>

无法解释他在自己的 DIY 数控路由器上看到的奇怪故障，[danil Van Den Berg]怀疑他的电子设备可能受到某种形式的电磁干扰(EMI)。于是他做了任何一个优秀的黑客都会做的事情，[翻遍零件箱，做了一个即兴 EMI 探测器](https://daniel.dmvandenberg.nl/diy-electromagnetic-interference-detector/)。

[丹尼尔]很快指出他不是电气工程师，也不保证他组装的小工具的准确性。但在他的测试中，它似乎工作得足够好，他能够识别特别“嘈杂”的电子组件，所以可能值得将一个放在一起，只是为了听听你的硬件向环境中注入了什么。

[![](img/211bd40849cc25ea3b1529dfe40a45b7.png)](https://hackaday.com/wp-content/uploads/2021/05/emiprobe_detail.jpg) 这里的硬件非常简单，[丹尼尔]只需用一个电阻将一圈实心铜线连接到 Arduino Nano 上的一个模拟引脚上，并在其中一个数字引脚上挂一个扬声器。从那以后，只需要几行代码就可以读取线圈中的电压，并将其转换成扬声器的音调。基本想法是，一个强大的交变磁场将在线圈中产生足够大的电压波动，以便 Arduino 的 ADC 进行读取。

如果你想更深入地了解你的电子产品可能会产生什么样的干扰， [[Alex Whittimore]在 2020 Hackaday Remoticon](https://hackaday.com/2021/01/08/remoticon-video-basics-of-rf-emissions-debugging-workshop/) 上发表了一篇精彩的演讲，内容是关于使用廉价的 RTL-SDR 加密狗进行射频调试。