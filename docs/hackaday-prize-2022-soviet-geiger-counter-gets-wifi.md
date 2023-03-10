# 2022 年黑客日奖:苏联盖革计数器获得无线网络

> 原文：<https://hackaday.com/2022/07/30/hackaday-prize-2022-soviet-geiger-counter-gets-wifi/>

[马莱克]有一个令人印象深刻的收集旧苏联风格的盖革计数器。在某些特定的情况下，这些都是方便的工具，但对我们大多数人来说，它们是稀奇的。即便如此，他们也需要来自现代世界的一些帮助才能很好地工作，而[Marek]已经想出了一些非常有创意的方法来将他们带入 21 世纪。比如这个版本，[增加了 WiFi 功能](https://hackaday.io/project/186444-wifigeiger)。

这是建立在 STS-5 盖革管的基础上，但真正的沉重的提升是由 ESP8266 处理的，它也提供无线网络连接。使用 ESP8266 来控制盖革管等对时间敏感的设备有一些限制，特别是缺乏本地存储，但[Marek]通过包括实时时钟和本地缓存数据直到重新建立网络连接来解决这个问题。该设备的未来计划包括增加温度和大气温度传感器。

最终，这个盖革计数器将被安装在一个防水的外壳中，这样[马雷克]就可以监视他的邻居的背景辐射。以前他用另一个版本做这个，但是那个版本[只能通过以太网电缆](https://hackaday.com/2019/02/13/a-network-attached-radiation-monitor/)访问网络，所以这个版本是一个相当大的升级。

[hack adayprize 2022](https://prize.supplyframe.com)主办单位:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)