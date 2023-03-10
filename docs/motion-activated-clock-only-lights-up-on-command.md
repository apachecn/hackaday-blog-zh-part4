# 运动启动时钟只有在收到命令时才会亮起

> 原文：<https://hackaday.com/2022/12/16/motion-activated-clock-only-lights-up-on-command/>

虽然我们中的一些人可以在任何地方睡着，从嘈杂的礼堂到灯火通明的火车站，但其他人更挑剔，需要安静和黑暗才能睡着。[克雷格·林德利]喜欢在睡觉时尽量减少光线，并决定给自己造一个简单的时钟，不会打扰他的休息。

基本的概念是建立一个时钟，只显示命令的时间。在这种情况下，命令将是在时钟前挥挥手。构建基于 Lilygo ESP32 T-Display 单元，该单元将 ESP32 与 LCD 显示器和电池管理系统相结合。ESP32 的 WiFi 连接通过查询 NTP 服务器提供准确的时间。被动红外运动传感器用于检测用户在时钟前的手的运动。

虽然市面上有各种各样的时钟和时钟收音机，但很少有运动激活的。[Craig]的工作很好地展示了如何构建自己的问题解决方案。我们以前也见过其他一些简洁的动作感应便利工具！