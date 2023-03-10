# NRF52 气象站发布时尚天气预报

> 原文：<https://hackaday.com/2021/03/11/nrf52-weather-station-gives-forecast-with-style/>

我们对围绕这些部分的 DIY 环境监视器并不陌生，事实上，这似乎是黑客在面对现代互联网连接的微控制器时最常见的项目之一。但是在这些项目中，这个由安德鲁·拉姆琴科建造的基于 nRF52 的微型气象站是我们见过的最精致的。

从外表上看，这似乎很容易成为一个商业产品。ePaper 显示器上的图形界面设计得非常好，在提供大量数据的同时，仍然具有足够的吸引力，可以挂在厨房里。外壳是 3D 打印的，但[安德鲁]在打磨和抛光正面时倾注了足够多的精力，你可能一眼看不出这一点。

[![](img/7a56668fed1ed7480e9b134b96a7e1f6.png)](https://hackaday.com/wp-content/uploads/2021/03/nrfweather_detail2.jpg) 在内部，它使用流行的 BME280 传感器来检测温度、湿度和大气压力，尽管定制的 PCB 也与类似的 SI7021 和 HTU21D 传感器兼容，如果你想改变事情的话。

也就是说，你真的想要测量压力的能力，因为它允许固件做自己的基本天气预报。所有收集的数据都通过蓝牙低能耗(BLE)传输出去，在那里可以由开源的 MySensors 物联网框架收集，但我们认为将它集成到您选择的家庭自动化系统中并不需要太多工作。

尽管我们可能对重新利用电子货架标签等东西的前景感到兴奋，但我们很高兴看到通用电子纸屏幕的价格最终下降到黑客群体可以负担得起这种规模的项目。

 [https://www.youtube.com/embed/0yZfeFMDKKY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0yZfeFMDKKY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

