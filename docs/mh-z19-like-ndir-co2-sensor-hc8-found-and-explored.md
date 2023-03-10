# 类 MH-Z19 NDIR CO2 传感器 HC8 的发现与探索

> 原文：<https://hackaday.com/2022/08/31/mh-z19-like-ndir-co2-sensor-hc8-found-and-explored/>

在寻找直接购买相当昂贵的 MH-Z19 二氧化碳传感器的替代方案时，[【spezifisch】偶然发现了一个“BreeRainz”品牌的小工具](https://spezifisch.codeberg.page/posts/2022-08-23/co2-sensor-reverse-engineering/)(也可以在其他品牌下找到)，它声称使用一个[【NDIR】](https://en.wikipedia.org/wiki/Nondispersive_infrared_sensor)(非分散红外)传感器来测量二氧化碳水平，而成本仅为€25。这种类型的传感器允许直接测量二氧化碳水平，而不是推断，使它们更加精确。

[![The BreeRainz DM1308A device cracked open.](img/7b68befb0484b5bb8b299334f02909ba.png)](https://hackaday.com/wp-content/uploads/2022/08/co2sensor-dis-1-0Y4IeYsmKL-orig.jpeg)

The BreeRainz DM1308A device cracked open.

打开这个小工具后(实际上，由于隐藏的螺丝)，二氧化碳传感器清晰可见。虽然表面上与 MH-Z19 相同，但 NDIR 传感器实际上被称为“HC8 ”,由广州海谷电子科技有限公司(广州顾海电子科技有限公司)。虽然与 MH-Z19 引脚兼容，但其 UART 协议并不相同。幸运的是，有数据表可以帮助实现它，这就是[spezifisch]所做的。

这就提出了一个问题，为了节省几欧元，像这样收集 NDIR 二氧化碳传感器是否值得。快速浏览一下德国亚马逊网站就可以发现，这款设备目前在€的售价为 35 英镑，而€的正品 MH-Z19 售价为 25 英镑甚至更低。还有很多 [MH-Z19 型号](https://emariete.com/en/sensor-co2-mh-z19b/) (B、C、D)，价格范围更广。所有这些都表明，在打折时找到一款包含 NDIR 传感器的设备可能会很有趣，但如果你只关心传感器本身，最好直接购买。