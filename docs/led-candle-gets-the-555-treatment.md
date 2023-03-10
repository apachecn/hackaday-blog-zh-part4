# LED“蜡烛”获得 555 待遇

> 原文：<https://hackaday.com/2018/09/05/led-candle-gets-the-555-treatment/>

经常阅读的读者可能记得，我们最近报道了一个巧妙的 Arduino 技巧，它允许你像吹灭蜡烛一样“吹灭”LED。这个想法是，LED 本身可以用作一个基本的温度传感器，当检测到其正向压降发生变化时，Arduino 代码会打开和关闭 LED。您需要对 Arduino 的 ADC 进行过采样，以可靠地检测几毫伏的变化，但总体而言，一旦您理解了原理，这就非常简单了。

[![](img/a9813fde3c85467534e8be834d4008f2.png)](https://hackaday.com/wp-content/uploads/2018/09/555candle_detail.jpg) 但是【Andrzej Laczewski】和我们许多亲爱的读者一样，觉得 Arduino 和其他微控制器如果被单独使用，可能会成为一个拐杖。[所以他开始用最珍贵的集成电路——555 定时器](https://bytechlab.com/2018/09/an-led-you-can-blow-out-like-a-candle/),复制这种黑客技术。在广告之后的视频中，他向那些认为控制 LED 的唯一方法是使用`digitalWrite`的人展示了他的“老派”LED 蜡烛。

并不是说用 555 复制原来的 Arduino 项目很容易，甚至很实用。[Andrzej]只是想表明这是可能的，这是我们在这些地区一直尊重的事情。他详细介绍了他是如何开发和测试该电路的，甚至包括示波器截图，显示了不同组件如何实时协同工作。但简而言之，MOSFET 用于打开和关闭 LED，比较器检测 LED 压降的变化，555 用于控制 LED 保持关闭的时间。

曾经的传统主义者，[Andrzej]用经典的激光调色剂转移方法的一种变体蚀刻他自己的 PCB，完成了这个构建。如果这一切对你来说看起来有点太像黑魔法，[坚持使用 Arduino 版本](https://hackaday.com/2018/08/21/an-led-you-can-blow-out-with-no-added-sensor/)也没什么丢人的。只需 1/20 的器件，无需校准，谁能说哪个版本“更简单”呢？

 [https://www.youtube.com/embed/pKUNnYLHodc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pKUNnYLHodc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

