# 用 Pi + MATLAB 实现人脸检测

> 原文：<https://hackaday.com/2020/08/04/facial-detection-with-pi-matlab/>

[Monica]想用她的树莓派尝试一下面部检测，她在 MATLAB 中找到了一些非常方便的包来帮助她做到这一点。这些软件包基于 [Viola-Jones 算法，这是第一个用于面部检测的实时对象检测框架](https://en.wikipedia.org/wiki/Viola%E2%80%93Jones_object_detection_framework)。

![](img/34bbaec69696c41b064ce7c8a814dad2.png)

她必须下载 MATLAB 的 Raspbian 映像，以便 Pi 能够通过自定义服务器解释 MATLAB 命令。这个设置非常简单，她在她的项目页面上很好地指导你完成了设置。

这样，现在她可以在 MATLAB 中控制 Pi:配置相机，切换 GPIO 等。真正的乐趣来自面部检测程序。除了打开 Pi 摄像机的实时视频输入外，该程序还输出像素数据。[Monica]主要是测试股票的能力，但接下来想尝试检测其他对象。我们会看看她能做出什么样的修改。

如果 MATLAB 不太符合你的口味，[我们在 Hackaday](https://hackaday.com/2011/05/16/cheap-and-reliable-portable-face-recognition-system/) 上有一系列[面部检测项目。](https://hackaday.com/2018/11/25/quick-face-recognition-with-an-fpga/)