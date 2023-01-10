# 使用移动传感器测量空气质量

> 原文：<https://hackaday.com/2021/12/13/measuring-air-quality-using-mobile-sensors-for-the-masses/>

空气质量差是全世界城市居民面临的一个主要问题。来自车辆、工业和农业的灰尘、烟雾、颗粒和有毒气体使许多大城市变得非常不适合居住。确定污染源和制定缓解策略需要污染物水平的准确数据，但获得这些数据并不总是容易的。

这是一个公民科学项目，旨在通过将传感器放在尽可能多的人手里来收集世界各地的空气质量数据。其团队为此开发了两种不同的传感器节点:一种是室内的[节点](https://canair.io/docs/canairio_co2.html)，可以测量一氧化碳 [2] ，另一种是移动的[，可以测量颗粒物(PM)水平。这两个版本都由 ESP32 微控制器驱动，该微控制器可以读取空气质量传感器，并使用 WiFi 或蓝牙连接到互联网。然后，这些数据可以在网上共享，以创建显示当地空气质量变化的详细地图。](https://hackaday.io/project/179753-canairio-bike)

传感器节点的设计是完全开源的，允许任何具有基本电子技能的人来构建它们。传感器是用于 CO [2] 测量的 Sensirion SCD30 和用于 PM 水平测量的 SPS30。移动版本带有一个整洁的 3D 打印外壳，可以安装在自行车的车把上，使用户能够快速收集他们周围的数据。一个移动应用程序简化了传感器的设置和数据共享。

该项目已经成功地在哥伦比亚的波哥大市收集了详细的数据，并且无疑将在世界各地的许多其他污染热点证明是有用的。我们已经看到类似的社区努力在不同的地方监测空气污染，甚至 T2 辐射，这两个例子都显示了相对简单的设备是如何有助于改善人们的福祉的。

 [https://www.youtube.com/embed/V2eO1UN5u7Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/V2eO1UN5u7Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

