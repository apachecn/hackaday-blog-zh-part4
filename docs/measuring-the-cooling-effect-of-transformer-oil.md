# 测量变压器油的冷却效果

> 原文：<https://hackaday.com/2018/11/15/measuring-the-cooling-effect-of-transformer-oil/>

变压器油长期以来有两个用途，冷却和绝缘。我们看到的连接到电网的大型钢制变压器充满了变压器油，通过散热片循环，将热量排放到周围的空气中。在黑客世界中，我们使用变压器油来冷却 RF 假负载和绝缘高压元件。[GreatScott]决定自己做一些测试，看看它对冷却回路有多好。

他开始测试芥花籽油，但发现它与空气接触后会分解，变得腐臭。所以他买了一些变压器油。首先，测试它对淹没电路的适用性，他发现当施加 15 V 电压时，无论他将触点放得多近，他都看不到任何高于电表 0.0 μA 限值的电流。在 1 cm 处，对于 115 Mohm/cm 的电阻，在 230 VAC 下，他获得了大约 2 μA，可能来自寄生电容。

接着进行热测试，他购买了一个 4.7 欧姆、100 瓦的散热器封装电阻，并用 Kapton 胶带将温度探头贴在上面。将它浸入变压器油中，连续施加 25 瓦的电流，七分钟后他测得温度为 46.8 摄氏度。使用蒸馏水进行的相同测试达到了 35.3°c。水的热容量为 4187J/kg K，毫不奇怪地比变压器油的 2090J/kg K 好得多，而变压器油的热容量是空气的 1005J/kg K 的两倍。

他做了更多的实验，但是我们将把这些留到他下面的视频中。

我们之前在各种油中运行过许多测试。例如，我们已经看到树莓 Pi 在[植物油](https://hackaday.com/2018/08/13/oil-immersed-raspberry-pi-keeps-its-cool-under-heavy-loads/)和[矿物油](https://hackaday.com/2017/05/15/liquid-cooling-overclocked-raspberry-pi-with-style/)中运行，以及[Arduino 在不导电的液体冷却剂](https://hackaday.com/2010/02/16/ultimate-flame-bait-liquid-cooled-arduino/)中运行，所有这些都不是超频就是在高负载下运行。

 [https://www.youtube.com/embed/78WgdXpAVxw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/78WgdXpAVxw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

