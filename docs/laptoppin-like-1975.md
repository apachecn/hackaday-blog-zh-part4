# 像 1975 年一样

> 原文：<https://hackaday.com/2022/08/06/laptoppin-like-1975/>

当我们第一次看到 [PZ1 笔记本电脑](https://hackaday.io/project/171471-pz1-6502-laptop)——一台 6502 笔记本电脑风格的电脑，配有一个小显示屏和 512K 内存——我们不禁想起了来自罗克韦尔的老式 [AIM 65](https://en.wikipedia.org/wiki/AIM-65) 电脑，尽管它只有 1K 的内存。AIM 没有的另一个东西是辅助微控制器，它比主处理器强大得多。

PZ1 实际上有几个版本，你可以在 Hackaday.io 和 [GitHub](https://github.com/NollKollTroll/PZ1_Pico) 上找到一些非常详细的信息。最近，[Adam]发布了 2.0 版本，并测试了一些运行良好的 PC 板。

当然，你需要软件。[Adam]已经移植了[Fuzix](https://hackaday.com/tag/fuzix/)的 nice。我们想知道罗克韦尔的设计师会如何看待如此奢侈的内存、SD 卡和更大的显示屏。他们可能会抱怨没有热敏打印机。

很多辅助功能都使用 Teensy 和 Arduino Nano。还有一个混合的树莓皮微微。这为显示器的未来升级提供了很多可能性。也许一个 ESP32 甚至可以把它放到 WiFi 上。

对于我们来说，当我们想玩 6502 代码时，我们会抓取一个 [Kim-UNO](https://hackaday.com/2014/11/07/the-kim-1-computer-minified/) ，即使它是仿真的。最近我们看到了很多 [6502 的活动](https://hackaday.com/2022/07/29/perseus-9-the-dual-6502-portable-machine-that-should-have-been/)。对于一个接近 50 岁的 CPU 来说，这已经不错了。