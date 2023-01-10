# 廉价的 ESP32 网络摄像头

> 原文：<https://hackaday.com/2019/02/02/cheap-esp32-webcam/>

想找一种便宜的方法来照看东西吗？[Kevin Hester]为我们指出了一种制作不到 10 美元的无线网络摄像头的方法。这使用了许多可用的廉价 ESP32 开发板之一，以及物联网平台 [PlatformIO](https://platformio.org/) 和一段[代码](https://github.com/geeksville/TenDollarWebcam)，创建了一个 RTSP 服务器。任何支持这种流媒体协议的软件都可以访问它，一点智能路由就可以把它放到互联网上。[Kevin]声称他使用的 ESP32 摄像机开发板不到 10 美元就能买到，但我们发现大多数板的价格约为[15 美元](https://www.banggood.com/TTGO-T-Journal-ESP32-Camera-Development-Board-OV2640-SMA-WiFi-3dbi-Antenna-0_91-OLED-Camera-Board-p-1379925.html?rmmds=myorder&cur_warehouse=CN)。无论哪种方式，这都比大多数商业流媒体相机便宜。

公平地说，这种黑客技术并不完全是脑外科手术:凯文所做的只是拿一块便宜的硬件，然后在上面安装一些开源软件。(编者注:但是凯文也写了开源软件！那次*是*脑外科手术。查看评论了解更多细节。)但有时这就是你所需要的，这将是一个制作网络摄像头的好方法，即使它被盗或损坏，你也不会失眠。

更新:我们应该澄清的是，脑外科手术比我们最初认为的要多一点:[凯文·赫斯特]实际上写了[微型 RTSP 库](https://github.com/geeksville/Micro-RTSP)使整个事情成为可能。他整洁的开源代码值得称赞！