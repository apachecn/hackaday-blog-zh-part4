# 一款小巧的低功耗壁挂式显示器

> 原文：<https://hackaday.com/2022/09/19/a-peppy-low-power-wall-mounted-display/>

[Phambili Tech]创造了一种电池供电的可安装显示器，称为[“the Newt”](https://github.com/Phambili-Tech/Newt_Display)，可用于显示时间、日历、天气或其他许多可定制项目的信息。

Newt 试图在保持高刷新率的同时提供长工作时间和具有丰富功能之间取得平衡。这种类型的许多电池供电设备使用 E-Ink 显示器，其提供长的操作窗口，但是刷新率差。Newt 使用 LCD 屏幕，虽然不像 E-Ink 显示器那样低功耗，但提供了更长的电池工作时间，同时仍然可以在日光下阅读，并提供高刷新率。

显示器本身是一个 2.7 英寸 240×400 夏普“像素内存”液晶显示器，在低功耗下提供生动的显示。Newt 通过其 ESP32-S2-WROVER 模块支持 WiFi，该模块具有 RV-3028-C7 实时时钟、用于声音反馈的蜂鸣器和用于输入和交互的电容式触摸传感器。据称，1.85 瓦时的 LiPo 电池(3.7V，500 毫安时)可以持续 1-2 个月，并且有可能使用更大的电池来延长寿命。

接收外部数据的不同功能通过编码到设备中的 [MQTT API](https://github.com/Phambili-Tech/Newt_Display/wiki/MQTT-API-Summary) 服务进行代理。一切都是开源软件和[开源硬件](https://github.com/Phambili-Tech/Newt_Display_Hardware)，包括[认证](https://certification.oshwa.org/us002116.html)，所以有事业心的黑客可以[将](https://github.com/Phambili-Tech/Newt_Display/blob/master/examples/Newt/Newt.ino)[服务](https://github.com/Phambili-Tech/Newt_Display/blob/master/src/Newt_Cloud/Newt_APIs.js)指向任何想要的东西，或者用他们自己的通信协议和功能扩展 Newt。

我们已经看到许多其他伟大的[壁挂式项目](https://hackaday.com/2020/11/03/e-paper-weather-display-is-a-great-base-to-build-from/)使用 [E-Ink 显示器](https://hackaday.com/2020/11/27/repurposing-large-electronic-price-tags/)，以及许多项目利用 [LCD 屏幕的高刷新率和低功耗](https://hackaday.com/2020/01/30/sma-q2-smart-watch-is-completely-hackable/)。我们希望看到更多的应用程序能够结合电子纸应用设备和使用液晶显示器的设备的最佳想法，同时仍然是开源的和对黑客友好的。

[https://player.vimeo.com/video/656242072?h=196bff1453&dnt=1&app_id=122963](https://player.vimeo.com/video/656242072?h=196bff1453&dnt=1&app_id=122963)