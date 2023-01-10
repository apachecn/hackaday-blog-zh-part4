# 无桥接器的 Homekit 兼容 Sonoff 固件

> 原文：<https://hackaday.com/2019/07/14/homekit-compatible-sonoff-firmware-without-a-bridge/>

一般来说，家庭自动化并不像大多数人希望的那样便宜或容易。有太多不兼容的协议，而且通常情况下，要让所有的东西都可以说话，需要你不情愿地注册一些你没有要求的“云”服务。如果你是一个苹果迷，可能会有更多的困难需要克服；让你的不受支持的智能家居设备与 Cupertino 设计的生态系统一起工作通常需要运行你自己的 HomeKit 桥。

为了尝试和简化事情，[Michele Gruppioni]为无处不在的 Sonoff WIFI 智能开关开发了一个[固件，允许它说本地 HomeKit](https://github.com/Gruppio/Sonoff-Homekit) 。不用再用一个覆盆子 Pi 来充当你的苹果硬件和那堆来自全球速卖通的 4 美元的 Sonoff 之间的调解人，他们现在可以直接相互交谈。在休息后的视频中，你可以看到 iPad 将 switch 识别为非官方设备，但由于它符合 HomeKit API，这并不妨碍他们相互通话。

这种麻省理工学院许可的固件不仅可以让你的 Sonoff Basic、Sonoff Slampher 或 Sonoff S26 与你的苹果小工具交谈，而且它还提供了一个 web 接口和 REST API，因此它可以与你在家庭自动化设置中运行的任何其他东西保持兼容。因此，虽然您的系统的普通用户可能会用他们的 iPhones 打开门廊灯，但您仍然可以按照自然规律用 Bash 脚本启动它。

当然，[如果你不介意在你的网络上不断增长的设备集合中添加一个 Raspberry Pi bridge](https://hackaday.com/2016/09/16/smartphone-tv-remote-courtesy-of-homekit-and-esp8266/) ，我们有大量的[其他 HomeKit 支持的项目供你查看](https://hackaday.com/2016/01/17/custom-siri-automation-with-homekit-and-esp8266/)。

 [https://www.youtube.com/embed/_PLeu4v50h0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_PLeu4v50h0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

