# 用于救援自主船只的太阳能自主拖船

> 原文：<https://hackaday.com/2021/09/18/solar-powered-autonomous-tugboat-for-rescuing-autonomous-vessels/>

[rctestflight]已经建造了几艘自主船，随着任务变得更长更具挑战性，他买了一艘充气皮艇作为专用的救援船。他建造了一艘[自主太阳能拖船](https://www.youtube.com/watch?v=fNxcOON1VNM)，而不是依靠过时的手动划桨。

![Towing test with kayak](img/334e1a24be4e16808851361c3435e74d.png)

♪ “Rum, treasure, ArduRover, Pixhawk 4 and so much solar, break of dawn till the day is over, the ship will surely go…” ♪

拖船在双体船配置中使用一对模制玻璃纤维船体。宽阔的平台允许在顶部安装一对 100 瓦的太阳能电池板。这是[rctestflight]第一次用玻璃纤维模制任何东西，所以有相当多的反复试验。模具被 3D 打印成部分，与定位销对齐，然后粘合在一起。环氧树脂固化后，两半模具可以分开，以便更容易地拆除船体。

与大多数[rctestflights]自动驾驶车辆一样，控制由运行 ArduPilot/ArduRover 的 Pixhawk 4 处理。一对由无刷电机驱动的 76 毫米黄铜螺旋桨提供推进和差速转向。电机由六块磷酸铁锂电池供电，电池通过 MPPT 充电控制器从太阳能电池板充电。船体覆盖着胶合板甲板，带有可移动的舱口和检查窗口。稍作调整后，他带着船进行了几次试航，最长的一次是 5.1 公里，由他自己驾着皮划艇。不到 5 公里/小时(3 英里/小时)，它不是快艇，但看起来肯定像一个放松的乘坐。[rctestflight]以前的许多船只都是气船，以避免让[水下推进器被杂草缠住](https://hackaday.com/2019/08/18/ardurover-boat-uses-to-float/)。这次问题不大，因为他可以把拖船拖近皮艇，清理螺旋桨。

[rctestflights]看起来总是既有趣又有教育意义，这部电影无疑为第二部中 13:32 的海底音乐设定了标准。

 [https://www.youtube.com/embed/fNxcOON1VNM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fNxcOON1VNM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/kWPgNLsfr8c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kWPgNLsfr8c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

