# 2022 年 Hackaday 奖:合理的流量帮助你跟踪你的用水量

> 原文：<https://hackaday.com/2022/10/17/2022-hackaday-prize-sensible-flow-helps-you-keep-track-of-your-water-usage/>

安全、清洁的饮用水是一种不应该被浪费的稀缺资源。但是当你打开水龙头时，并不总是容易看到你用了多少:是一分钟一升吗？十点了吗？洗手或者刷牙的时候实际用了多少？如果你想获得一些关于你的用水量的可靠数据，看看[【乔希·EJ】的“合理用水项目](https://hackaday.io/project/182279-sensible-flow)”。它包含了一组传感器的设计，可以测量你的耗水量，还有一个方便的小显示屏，可以显示总耗水量。

测量用水量最明显的方法是在你的管道上安装现成的流量计，这是可感知流量支持的。但这个项目最有趣的部分可能是一种非侵入式流量传感器的设计，你可以简单地将其连接到任何类型的水龙头上。这款传感器包含一个九轴惯性测量单元(IMU)，可以检测您扭曲、转动或倾斜手柄的程度，并使用这些信息来估计水流量。你需要使用计时器和量杯进行初始校准步骤，但你不必为了记录用水量而拆开水管。

这两种类型的传感器都由硬币电池供电，估计可以工作大约一年，这要归功于高能效的 Arduino Pro Mini 和与基站通信的蓝牙低能耗(BLE)模块。基站插在墙上的插座上，在一个一英寸的小有机发光二极管显示器上显示总用水量。外壳的 STL 文件可在项目页面上获得，以及显示所有部件如何连接的详细电路图。

我们已经看到了几种家用水流测量系统，例如[这种基于 ESP8266 的简洁淋浴水监控器](https://hackaday.com/2022/08/26/water-monitor-measures-the-cost-of-your-shower-thinking-time/)。如果你喜欢一个简单的关闭水龙头的视觉提示，看看[这个 LED 小工具](https://hackaday.com/2014/08/19/faucet-add-on-attempts-to-save-water-by-changing-colors/)。

 [https://www.youtube.com/embed/9RIbbollBk8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9RIbbollBk8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[hack adayprize 2022](https://prize.supplyframe.com)主办单位:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)