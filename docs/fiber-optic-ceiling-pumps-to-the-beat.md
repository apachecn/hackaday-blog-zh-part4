# 光纤天花板泵的节拍

> 原文：<https://hackaday.com/2020/06/17/fiber-optic-ceiling-pumps-to-the-beat/>

多年来[森塔斯]的梦想是把星星带到他的家，并建立一个光纤天花板。尽管市面上有许多光纤星形天花板套件，但我们很高兴他决定在这个项目上完全 DIY，因为[结果简直令人震惊](https://www.instructables.com/id/Fiber-Optic-Star-Ceiling-Music-Reactive/)。

[Centas]选择制作一个从他家可以看到的部分天空的模型，并用天文馆软件 [Celestia](https://celestia.space/index.html) 生成了一张 1200 颗星星的地图。制作星形天花板最耗时的部分总是要为纤维戳很多孔。在[Cenas]的案例中，这被证明是特别麻烦的，因为他决定在悬挂天花板后安装光纤，所以他想出了一种方法，在从底部推动光纤后用鱼竿抓住光纤。完工的天花板看起来真的很棒，虽然它的圆形边缘包含 RGB LED 灯条，用于侧面照明。[Cenas]还在安装光纤后粉刷了天花板，这样当它们不亮时就看不见了，但仍然有足够的光线穿过油漆。

电子设备被分成两部分，一部分是安装在激光切割盒中的发射器，另一部分是直接安装在天花板上的接收器。发射机包含一个 MSGEQ7 图形均衡器芯片和一个音频插孔，使天花板听起来有反应。

控制方案有些不同寻常，因为发射器从红外遥控器接收信号，然后通过 NRF24L01 2.4 GHz 模块将信号转发给接收器。接收器模块通过连接到一些晶体管和 MOSFETs 的 PCA9685 PWM 控制器来调节 led 亮度。该电路实际上造成了一些问题，因为 led 在低 PWM 值时开始闪烁。显然，这是由 MOSFETs 的低开关时间引起的，因此[Cenas]通过降低 PWM 频率来解决这一问题。

在下面的视频中，看起来[Cenas]也安装了一些照明设备，可以在星座之间画出线条，但在评论中，他透露这只是通过视频编辑完成的。不过，如果能看到有人使用 LED 灯条或侧面发光光纤来制造这种照明，那就太好了。

有趣的是，其他人已经找到了类似的安装方法，他们从 T1 楼上的房间直接将光纤穿过天花板。

 [https://www.youtube.com/embed/CcMFqSMNY2w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CcMFqSMNY2w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

