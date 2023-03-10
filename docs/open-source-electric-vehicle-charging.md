# 开源电动汽车充电

> 原文：<https://hackaday.com/2021/04/06/open-source-electric-vehicle-charging/>

电动汽车在路上越来越常见，但当它们停在车道或车库时，充电时仍有一些问题需要解决。当然，市场上有很多充电站，但它们都有不同的特性、功能，甚至端口，所以要真正确保对汽车电池充电的完全控制，可能有必要把手伸进零件箱，拿出一个可信赖的 Arduino。

[这个项目由【Sebastian】](https://dehnes.com/electronics/2021/03/31/dehneevse_charging_station.html)提供给我们，他需要对他的 Leaf 充电进行这种级别的控制，并且他也有能力实施这个项目，从大型高压开关接触器到运行其网络连接和 web 应用程序的软件。这个充电站也有所有可用的功能。它可以告诉汽车以不同的速率充电，并可以限制它在不同的时间充电(例如，如果能源在晚上更便宜)。它能够通过通信总线监控汽车的充电状态和其他信息，甚至有一个前端 web 应用程序来监控和控制设备。

该项目基于 Arduino Nano 33 物联网，所有代码可在[项目的 GitHub 页面](https://github.com/sebdehne/DehneEVSE-Firmware)上获得。虽然我们建议在处理电源电压和与电动汽车这样的高价产品接口时要非常小心，但乍一看，这款车似乎已经通过了所有的测试，甚至可能成为未来生产单元的良好原型。如果你不需要这个充电站拥有的所有功能，[你可以随时黑掉汽车本身来增加一些更先进的充电功能](https://hackaday.com/2020/09/12/adding-luxury-charging-features-to-an-entry-level-ev/)。

 [https://www.youtube.com/embed/G5hRH6UQRbQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/G5hRH6UQRbQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

