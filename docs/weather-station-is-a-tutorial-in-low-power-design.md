# 气象站是低功耗设计的教程

> 原文：<https://hackaday.com/2018/11/04/weather-station-is-a-tutorial-in-low-power-design/>

建立自己的气象站本身是一个有趣的项目，但建立一个自给自足、远离电网的气象站又增加了一系列挑战。你需要一个电池和一个太阳能电池板来给这个站供电，这意味着至少要给你的建筑增加一个调节器和充电控制器。如果面板和电池很小，你还需要[对代码做一些节能调整](https://www.danilolarizza.com/stazione-meteo-solare-wifi-v2-0/)。([谷歌翻译](https://translate.google.com/translate?sl=auto&tl=en&js=y&prev=_t&hl=en&ie=UTF-8&u=https%3A%2F%2Fwww.danilolarizza.com%2Fstazione-meteo-solare-wifi-v2-0%2F&edit-text=&act=url)来自意大利语)【达尼洛·拉里扎】在他的建筑中使用的技巧不仅对气象站有用，它们对任何试图优化他们的离网项目的电池和太阳能电池板尺寸的人来说都是完美的。

说到节能，先摘下低垂的果实。[Danilo]将测量间隔设置得尽可能长，并使微控制器(NodeMCU)在其间休眠。当微控制器休眠时，切断传感器的电源是另一个简单的步骤，但该设备仍然会在一夜之间崩溃。然后，他转向硬件解决方案，并在设置中添加了更高效的电池充电器，从而节省了更多的电力。这更加令人印象深刻，因为该站通过 WiFi 进行通信，众所周知，在低功率应用中很难运行。

除了低功耗优化，气象站本身也因其相对简单而有趣。它可以用我们大多数人身边的东西来建造。最棒的是，[Danilo]在他的网站上发布了源代码，所以大部分艰苦的工作已经完成了。如果你觉得他有点眼熟，那是因为我们之前报道过他的一些项目，比如他的[廉价 WiFi 延长天线](https://hackaday.com/2012/11/27/cheap-biquad-antenna-extends-lan-between-apartments/)和他的[自制混合电子管放大器](https://hackaday.com/2012/12/04/cute-little-amplifier-has-a-tube-pre/)。