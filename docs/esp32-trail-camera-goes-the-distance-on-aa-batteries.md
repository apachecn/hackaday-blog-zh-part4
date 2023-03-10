# ESP32 拖车摄像机使用 AA 电池

> 原文：<https://hackaday.com/2020/05/18/esp32-trail-camera-goes-the-distance-on-aa-batteries/>

ESP8266 和 ESP32 不乏令人喜欢的地方，但如果我们必须列出这些支持 WiFi 的微控制器必须提供的最佳功能，它们的电源管理功能肯定会名列前茅。这就是我们如何假设[【马克】能够用他的 ESP32 相机](http://marksbench.com/electronics/esp32-cam-low-power-trail-camera/)拍摄多达 23，475 张照片，而他的电源只不过是杂货店里的四节 AA 电池。

[![](img/69b1ddb99b0226fe3fe765592c41e2db.png)](https://hackaday.com/wp-content/uploads/2020/05/esp32cam_detail.png) 但事实证明，整个故事颇有点意思。据我们所知，[Mark]并没有为 ESP32 的睡眠模式而烦恼。事实上，看起来你可以用任何你想要的芯片来完成这个把戏，这当然使它值得在心里为未来存档；即使它依赖于一个相当具体的用例。

用最简单的话来说，当 ESP32 不主动拍照时，[马克]就完全切断了它的电源。他发明的巧妙电路只有在 PIR 传感器检测到摄像机前方有物体移动时才会开启微控制器。一旦芯片上电并运行代码，它会将其中一个 GPIO 引脚拉高，进而触发连接到电路 MOSFET 栅极的 4N37 光隔离器。只要引脚保持高电平，电路就不会切断 ESP32 的电源。这使得芯片有时间拍摄所需数量的图片，并在将引脚拉低并允许电路拔掉插头之前将一切整理好。

如果您希望在不与任何 MOSFETs 发生冲突的情况下最大限度地提高运行时间，我们已经看到了一些优秀的示例[，说明如何充分利用 ESP8266 和 ESP32 上的低功耗模式](https://hackaday.com/2017/09/24/datalogger-uses-esp32-and-esp8266-low-power-modes/)。

感谢杰森的提示。]