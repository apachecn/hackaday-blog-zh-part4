# 两部分，四线空气质量计显示如何做到这一点

> 原文：<https://hackaday.com/2020/08/25/two-part-four-wire-air-quality-meter-shows-how-its-done/>

[![](img/8a7437c793d02336293d5ca201dc4fe4.png)](https://hackaday.com/wp-content/uploads/2020/08/ESP32-BME680-Square.png) 博世 BME680 是一个超级功能的环境传感器，【随机书呆子教程】已经[将其与 ESP32 结合，创建了一个空气质量计，它不仅可以作为一个很好的教程](https://randomnerdtutorials.com/esp32-bme680-sensor-arduino/)，不仅可以让传感器启动和运行，还可以设置一个简单的(和可选的)网络服务器来提供读数。这是一个伟大的项目，从头到尾一步一步地完成所有事情，包括如何安装必要的库以及如何对 ESP32 进行编程，因此对于任何想学习的人来说，这是一个完美的周末项目。

BME680 是一款小型器件，通过 SPI 或 I2C 进行通信，集成了气体、压力、温度和湿度传感器。气体传感器部分检测各种挥发性有机化合物(VOCs)和污染物，包括一氧化碳，这使其成为一种有用的室内空气质量传感器。它仅提供相对测量值(较低的阻力对应于较低的空气质量)，因此为了获得最佳结果，应根据已知的来源进行校准。

[![](img/d29dd2261f794ad2eb3a5dc173b49c06.png)](https://hackaday.com/wp-content/uploads/2020/08/ESP32-BME680-Serial.png) 本教程使用 Arduino IDE 及其附件来支持 ESP32 和 Adafruit 的库。不熟悉这种东西？本教程介绍了两者的安装过程。有对源代码的很好的解释，以及输入设置值(如当地气压，海平面的函数)以获得最佳结果的指导。

一旦软件安装在 ESP32 上，就可以从串行端口监视器中读取结果。通过更进一步，ESP32 可以运行一个小型 web 服务器(使用 [ESPAsyncWebServer](https://github.com/me-no-dev/ESPAsyncWebServer) )以无线方式向任何设备提供数据。这是一个写得很好的教程，涵盖了每个元素，[补充了另一个基于 BME680 的空气质量计，它使用 MQTT 和 Raspberry Pi](https://hackaday.com/2020/07/20/a-portable-home-air-quality-meter-with-the-esp32/) 。