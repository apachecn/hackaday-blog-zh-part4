# 自定义天气相机饲料与软件技巧

> 原文：<https://hackaday.com/2020/07/23/custom-weather-camera-feed-with-software-tricks/>

有了意大利海边的美丽景色，我们并不惊讶(Danilo Larizza)设置了几个 IP 摄像机来捕捉实时视图。但是使用一个树莓 Pi，一个环境传感器，和一些软件欺骗来覆盖当前的(自然的，完美的)天气状况在图像上？现在他只是在戏弄我们。

不管他的动机是什么，我们不得不承认最终的结果是非常好的。尤其是当您发现这里没有复杂的硬件或软件在工作时。一个原始的 Raspberry Pi 完成了所有繁重的工作，它使用`ffmpeg`从外部 IP 摄像机中提取一帧，使用 Python 脚本轮询与 I2C 连接的 BME280 温度和湿度传感器，然后使用 ImageMagick 生成环境数据覆盖其上的最终快照。

[Danilo]给出了他在该过程的每一步中所使用的确切命令，这使得很容易跟随并看到最后一切是如何组合在一起的。如果你想的话，这也会让你更容易适应自己的目的。一旦你看到所有的部分是如何组合在一起的，那么数据和图像的来源就取决于你了。

我们之前已经展示了如何使用一些简单的 [Python 代码将您的原始数据转换成吸引人的图像](https://hackaday.com/2018/03/21/making-pictures-worth-1000-words-in-python/)，并且将它与真实世界的照片相结合是将充满价值的文本文件转换成值得炫耀的展示的极好方式。