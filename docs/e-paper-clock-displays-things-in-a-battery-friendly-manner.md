# 电子纸时钟以电池友好的方式显示事物

> 原文：<https://hackaday.com/2022/05/15/e-paper-clock-displays-things-in-a-battery-friendly-manner/>

时钟构建是黑客的主食，许多溢出与耗电的 led 和网络功能。来自[mattwach]的这款产品采取了完全相反的方法，由于基于电子纸的设计，它可以消耗电池。

该构建依赖于一个小型 Waveshare 电子纸模块，该模块仅在显示器实际变化时才需要电力。当静止时，显示器不需要电力，与有机发光二极管或基于 LCD 的时钟相比，这有助于节省大量电力。

Atmega328p 是该产品的核心，运行 32.768 KHz 时钟晶体，以实现精确计时和低功耗的结合。由于 GPS 模块允许时钟在通电时与卫星时间同步，因此确保了时间的精确*和*。[这是一种将时钟同步到高质量时间源的常见方式](https://hackaday.com/2021/07/25/portable-gps-time-server-powered-by-the-esp8266/)。然而，大多数时候，GPS 保持断电，以节省模块在使用时通常消耗的 30-100 mA。

其他功能包括温度、湿度和压力传感器，以及随时间变化的环境压力图表。还有日出和日落时间的通知，以及月亮的当前相位。它被包装在一个使用 3D 打印部件和一些木制 CNC 切割面板优雅制造的箱子中，具有漂亮的乡村风格。

随着电子纸显示器和微控制器配置为低功耗运行，时钟将在四个 AAA 电池上运行约 6 个月。总的来说，这是一个漂亮的小时钟，它将提供时间，日期和其他信息，而不需要互联网连接。休息后的视频。

 [https://www.youtube.com/embed/99J65S5GTPI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/99J65S5GTPI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

