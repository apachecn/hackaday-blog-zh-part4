# 只用一个 Arduino 和一根电线测量电磁场

> 原文：<https://hackaday.com/2022/04/17/measuring-electromagnetic-fields-with-just-an-arduino-and-a-piece-of-wire/>

电磁干扰问题是一个很难调试的问题。如果您需要证明是什么原因导致您的 WiFi 变慢或您的数字电视信号下降，那么测量电磁场(EMF)的能力可以提供很大的帮助。专业设备往往非常昂贵，但自己制作一个电动势检测器甚至没有那么困难:只需看看 Arduino 专家【Mirko Pavleski】的[便捷手持电磁场检测器](https://hackaday.io/project/184892-arduino-emf-electromagnetic-field-detector)就知道了。

基本想法非常简单:将天线直接连接到 Arduino 的模拟输入端，并观察它测量的信号。由于 ADC 的输入为高阻抗，因此它对天线拾取的任何杂散电流都非常敏感。事实上非常敏感，需要一个几兆欧的接地电阻来防止传感器被任何随机噪声触发。[Mirko]通过几个旋钮和开关使电阻可调，这样探测器就可以在安静和嘈杂的环境中使用。

让整个设备可靠地工作是电磁工程中一项有趣的工作:在最初的几次迭代中，探测器会触发自己的发光二极管和蜂鸣器，陷入永无止境的循环中。[Mirko]通过将 Arduino 封装在一个封闭的接地金属盒中，只露出所需的电线，解决了这一问题。天线的设计很大程度上是基于反复试验；具有 7cm×3cm 铝片的当前设置似乎工作良好。

虽然这不是一个经过校准的专业级仪器，但它应该可以方便地找到干扰源，甚至只是找到隐藏的电源电缆。你可以把这看作是[【Mirko】的垃圾箱电动势检测器](https://hackaday.com/2022/01/10/a-simple-emf-detector-and-electroscope-you-can-make-from-junk-box-parts/)的更高级版本；如果你身边有第二个 Arduino，你可以用那个[代替](https://hackaday.com/2014/03/18/listening-to-electromagnetic-interference-with-a-rtlsdr-dongle/)来产生干扰。

 [https://www.youtube.com/embed/gVDJj16gzY0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gVDJj16gzY0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

