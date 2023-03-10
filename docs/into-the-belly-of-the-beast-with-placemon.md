# 把胎盘放进野兽的肚子里

> 原文：<https://hackaday.com/2020/09/17/into-the-belly-of-the-beast-with-placemon/>

不，不，起初我们也认为它是一个口袋妖怪，但是 Placemon *mon* 代表你的*地方*，你的家，你的住所。这不是像一氧化碳探测器或防盗报警器这样的专用设备，而是一个[通用监控器](https://hackaday.io/project/173368-placemon-sense-your-home)，它将数据传输到中央处理器，如果有什么不对劲，机器学习算法会通知你。在某种程度上，它就像一只看门狗，如果你的地方异常寒冷、着火、被非法占据或在水下，它会给你发短信。

【错综复杂】正试图基于一篇关于通用传感的科学论文的灵感，制造一个对黑客友好的版本，它将拥有更便宜的组件，但会失去准确性。例如，文章建议热电堆阵列，如低分辨率热视觉，但 Placemon 将有一个温度计，这似乎是一个谨慎的起点。

PCB 已准备好开始收集声音、温度、湿度、气压、照明和被动红外，然后使用 Wifi 通过板载 ESP32 报告遥测数据。一个利用 Tensorflow 的盒子接收来自任意数量位置的数据，并正在训练识别一些日常家居事件的传感器签名。训练从容易重复的事件开始，比如厨房的声音和电器操作。从那时起，[anfractuosity]希望他能精通到教它新的声音，所以如果有宠物加入，它不会认为每次 Fluffy 需要去洗手间时都会有雪崩。

我们还有另一个杰出的例子，即[在不直接与电器接口的情况下感知家庭事件](https://hackaday.com/2020/07/17/home-monitoring-without-all-the-sensors/)，而[将传感器套件带到你的汽车上](https://hackaday.com/2016/12/06/homebrew-dash-cam-enables-full-suite-of-sensors/)可能是你的拿手好戏。

The [HackadayPrize2020](https://prize.supplyframe.com) is Sponsored by:[![Supplyframe](img/193ca31946d20fcfa39296cb816a4c50.png)](https://supplyframe.com/)[![Digi-Key](img/4fc24a8a6b4498aecfe987b00009d192.png)](https://www.digikey.com/)[![Microchip](img/8dd361210bbb0e5592c24f87e4e2267e.png)](https://www.microchip.com/)[![Arm](img/7d728b281b85469ef9013d45001f14b4.png)](https://www.arm.com/)