# 可视化飞机跟踪器在 Pi 上运行

> 原文：<https://hackaday.com/2019/01/11/visual-airplane-tracker-runs-on-pi/>

毫无疑问，对于许多读者来说，在撰写本文的地方附近，有一个 Raspberry Pi 正在运行，它可以跟踪飞机，收听飞机发送的 ADS-B 无线电广播，并将数据上传到共享服务。不过，这款设备缺少黑客定制声明中应有的闪亮发光二极管。来自[xy72y5e]的这个项目将是解决这个问题的一个很好的方法:他们使用一顶独角兽帽来创建一个当地飞机的简单地图。这在[独角兽帽](https://shop.pimoroni.com/products/unicorn-hat)的 8x8 RGB LED 矩阵上显示了该区域飞机的位置和轨迹。

虽然这里的设备根据他们的无线电定位来绘制当地飞机的地图，但[xy72y5e]发布的代码可以与 ADSBExchange 的 [api 一起工作，ADSBExchange](https://public-api.adsbexchange.com/)是一个共享飞行数据的网站。这意味着地图可以很容易地设置为显示设备本身不同位置的空中交通。改变这一点以显示本地检测到的平面并不困难，因为[xy72y5e]已经发布了创建地图的[完整 Python 代码。这也将与我们最近看到的其他一些飞机跟踪黑客配合得很好，例如](https://github.com/x72y5e/radar)[飞机观察者目的地跟踪器](https://hackaday.com/2016/07/17/planespotter-spots-planes-tracks-destinations/)或[通过雷达反射跟踪飞机](https://hackaday.com/2018/10/11/studying-airplane-radio-reflections-with-sdr/) …

[Via [Reddit](https://www.reddit.com/r/raspberry_pi/comments/aei4fb/visual_aircraft_tracker_on_raspberry_pi/)