# 这个 Chromecast 音量旋钮有一种 70 年代的时尚

> 原文：<https://hackaday.com/2019/01/31/this-chromecast-volume-knob-has-a-certain-70s-chic/>

在过去的几年里，Chromecast 设备已经在世界各地的家庭中流行起来。它们使得从智能手机或笔记本电脑向连接到同一网络的一组扬声器或显示器播放音频或视频变得容易。[Akos]希望通过一个简单的设备来控制这些设备的音量，而不是总是使用智能手机。这样就造出了 [CastVolumeKnob。](https://hackaday.io/project/163525-castvolumeknob)

该项目从使用 Wireshark 捕获 pychromecast 库发送的数据开始。一旦[Akos]理解了消息格式，这就在 ESP8266 上的 MicroPython 中实现了。旋转编码器被用作音量旋钮，Neopixel 环被用于关于被控制的设备和当前音量水平的视觉反馈。

为了提高可用性，还做了进一步的工作，ATtiny85 微控制器用于在唤醒 ESP8266 之前监控编码器的按钮按压，从而大大降低功耗。该设备也是可充电的，这要归功于 18650 锂聚合物电池、充电器和升压转换器板。这一切都被包裹在一个光滑的 3D 打印外壳中，半透明的 led 边框和时髦的加工铝旋钮作为顶部的樱桃。

这是一个自制的设备，但在客厅环境中既时尚又不显眼。我们认为，当有重要的电话打进来，需要把立体声调到更合适的音量时，它非常有用。

再来一张，[看看这个 USB 音量旋钮，它有一种很好的重量感，由 lead shot 提供。](https://hackaday.com/2016/01/06/pump-up-the-volume-with-lead-shot-and-leds/)