# unifiedwater 发现可饮用水并阻止污染者

> 原文：<https://hackaday.com/2020/08/29/unifiedwater-finds-potable-water-and-stops-polluters/>

全世界数百万人无法获得干净的饮用水，这主要是因为企业和个人造成的污染。解决这个问题需要一种负担得起的、可扩展的方法来快速判断水质，打包数据，并在证据消失之前将其提交给能够打击污染者的权威机构。理想情况下，解决方案应该是开源的，并且易于复制。公民科学家越多越好。

安德烈·弗洛里安的《统一的水》直接来源于这一思路。[将这个小型手持设备浸入水面以下，它会快速采集一系列水质和大气读数，对它们进行平均，然后使用 Arduino MKR GSM 将数据发送到网络仪表盘](https://hackaday.io/project/174026-unifiedwater)。

UnifiedWater 通过测试水的 pH 值和浊度来判断水质，从而测量杂质的含量。商业浊度传感器通过测量液体中存在的固体散射的光量来工作，因此[Andrei]用一个指向光电池的 LED 自制了一个版本。UnifiedWater 还读取空气温度和湿度，并报告其位置和时间戳。

该器件可以在两种模式下运行，具体取决于应用。企业模式是为策略性地放置在水体周围的一组设备而设计的。在这种模式下，设备连续采样，每 15 分钟读取一次读数，并可以发送在预定义阈值时触发的通知。对于需要寻找饮用水的徒步旅行者和露营者来说，还有一种一次性的个人模式。一旦 UnifiedWater 读取了读数，NeoPixel 环就会提供即时的颜色编码判断。休息后请欣赏演示。

 [https://www.youtube.com/embed/887ubuvnKtg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/887ubuvnKtg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[hack adayprize 2020](https://prize.supplyframe.com)主办单位:[![Supplyframe](img/193ca31946d20fcfa39296cb816a4c50.png)](https://supplyframe.com/)[![Digi-Key](img/4fc24a8a6b4498aecfe987b00009d192.png)](https://www.digikey.com/)[![Microchip](img/8dd361210bbb0e5592c24f87e4e2267e.png)](https://www.microchip.com/)