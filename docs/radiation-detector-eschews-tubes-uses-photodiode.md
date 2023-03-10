# 辐射探测器避开电子管，使用光电二极管

> 原文：<https://hackaday.com/2019/02/22/radiation-detector-eschews-tubes-uses-photodiode/>

当话题是辐射探测时，人们自然会想到古老的盖革-米勒管。它已经存在很长时间了，俄罗斯剩余的管子几乎不需要任何东西就能买到，而且很容易使用。但作为真空管，它可能有些脆弱，运行它所需的高电压可能有点危险。

幸运的是，有其他方法可以看到放射性世界发生了什么，比如这个半导体辐射探测器。[Robert Gawron]在建造了几个 G-M 管探测器后，建造了它作为概念验证。他的固态设计依赖于一个反向偏置的光电二极管，当电离辐射击中 pn 结时，光电二极管导通。微小信号由一对低噪声运算放大器放大，并输出到 BNC 连接器。传感器的模拟输出发送到示波器，示波器的触发输出连接到一个用于数据采集的核子板。Nucleo 又连接到一个 Raspberry Pi，用于累计和记录。这是一个复杂的链，但传感器似乎是有效的，甚至可以检测到钍钨电极的α辐射，这是我们无法用 G-M 管计数器复制的壮举。

[罗伯特]的固态探测器可能不是最佳的，但它有前途。我们以前也见过 [PIN 二极管被用作辐射探测器](https://hackaday.com/2014/10/25/use-a-cheap-pin-diode-as-a-geiger-counter/)。

[via [危险原型](http://dangerousprototypes.com/blog/2019/02/19/semiconductor-radioactivity-detector-part-2/)