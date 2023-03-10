# 灯丝干燥箱的设计太过了

> 原文：<https://hackaday.com/2022/02/15/filament-dry-box-design-goes-way-over-the-top/>

当涉及到项目设计时，简单的功能蠕变和超越极限之间有一条细微的界限。很难说那条线到底在哪里，但我们很确定这个灯丝干燥箱至少跨过了它，甚至可能完全抹去了它。

当然，我们都知道在受控条件下储存 3D 打印机灯丝的价值，以防止吸湿塑料吸收大气中的水分。但是[马赛丽·卡拉诺维奇]一定非常非常讨厌由此产生的印刷艺术品。从一个已经有内置加热元件的商用干燥箱开始，[马赛丽]通过用 ESP32 替换控制器和显示器将它带到了一个新的水平。他增加了一个风扇，以改善外壳内的空气循环，防止分层，以及温度和湿度传感器。他不满足于简单地在特定的设定点打开和关闭加热元件，他还实现了一个 PID 回路来保持恒定的温度。当然，还有 web UI 和 API 可用于第三方控制和监控。

下面的视频详细介绍了[马赛丽]的设计思想，并深入到建筑和性能的一些细节。虽然我们可能会开玩笑说这种设计有些夸张，但真正的意思是，这不仅是一个应用程序设计思想的展示，也是整个硬件项目设计思想的展示。当然还有更简单的加热干燥箱设计和零成本解决方案，但有时走极端也有其价值。

 [https://www.youtube.com/embed/txF2oQPIjb4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/txF2oQPIjb4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

