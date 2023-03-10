# 无线低功耗 E-Ink 天气小工具

> 原文：<https://hackaday.com/2021/03/02/wireless-low-power-e-ink-weather-gadget/>

不久前，制作一个配备电子墨水屏幕的低功耗无线天气显示器需要大量的工作，而且几乎肯定会比[Dmitry]创造的设备更大。

[![](img/d1cb2e7da3d51d8f9752abe990293a05.png)](https://hackaday.com/wp-content/uploads/2021/02/weather3.jpg)

(1) Weather alert indicator, (2) Current temperature, (3) Humidity and wind, (4) 24-hour temperature graph, (5) 24-hour precipitation probably graph

他的低功耗电子墨水天气小工具利用了一个 niftier 开发板，创造了一个有用而纤薄的设备，完全满足了他的需求。在网上查天气很快，但不如在方便的地方看一眼显示屏快。

[Dmitry]选择的主板是 LilyGO TTGO T5s，这是一种基于 ESP32 的主板，集成了电子墨水显示器，除非更新，否则不需要电源。它已经加载了足够的智能来使用 [OpenWeather API](https://openweathermap.org/) 获取天气信息，并相应地更新显示。

打开 WiFi 获取一个容易解析的 JSON 文件并每小时更新一次显示意味着电池可以提供几个月的运行时间。作为奖励，LilyGO 板甚至包括给电池充电的功能，这让事情变得非常方便。

材料清单在这里，设备的代码，包括安装说明，在项目的 [GitHub 库](https://github.com/dmi3/weather)上。如果你的品味碰巧更倾向于艺术而非实用，[我们正好为你准备了天气预报。](https://hackaday.com/2020/05/19/weather-display-is-cloudy-with-a-chance-of-esp8266/)