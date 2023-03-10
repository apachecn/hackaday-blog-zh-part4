# ESP32 获得了一个漂亮的串行控制台库

> 原文：<https://hackaday.com/2022/07/22/esp32-gets-a-nifty-serial-console-library/>

有时候你需要找个项目跟你聊聊，这样你才能看到里面的情况。来自[jbtronics] [的 ESP32 控制台 Arduino 库承诺了这一点。](https://github.com/jbtronics/ESP32Console)

该库为 ESP32 添加了一个简单的串行控制台，并与 Arduino 生态系统兼容。它允许轻松添加自定义命令，因此您可以调整控制台以适应您自己的项目。它还具有非常完美的特性。有自动完成和可导航的命令历史——这是你只能从现代操作系统终端中期待的功能。还内置了一些系统命令，用于检查内存、网络接口等的状态。

该工具可通过 Arduino 库管理器或 [PlatformIO 注册表获得。](https://registry.platformio.org/libraries/jbtronics/ESP32Console)您可能希望将它与兼容 VT-100 的终端(如 PuTTY 或类似设备)配合使用，这样您就可以使用包括彩色输出在内的所有奇特功能。[jbtronics]也希望很快将其移植到 ESP8266 上！

最近，我们也看到了一些其他伟大的系列工具。如果你正在酝酿自己漂亮的控制台黑客，[一定要给我们写信！](http://hackaday.com/submit-a-tip)