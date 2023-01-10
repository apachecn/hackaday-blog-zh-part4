# MQTT 仪表板使用夏普记忆液晶显示器

> 原文：<https://hackaday.com/2020/11/29/mqtt-dashboard-uses-sharp-memory-lcd/>

目前更有趣的显示技术之一来自夏普，他们的记忆显示设备具有电子墨水显示器的低功耗优势，更新速度快得多，我们可以期待液晶显示器或类似设备。由于成本原因，我们在我们的社区中并没有看到多少，所以很高兴看到一个用于来自[Raphael Baron的 MQTT 仪表板项目中。

硬件将显示器放在一个相对简约的 3D 打印外壳的顶部，后面是 LOLIN32 ESP32 开发板，前面是一个包含小型旋转编码器和三个 clicky 按键开关的底座。令人惊讶的是，该项目的最有趣的部分并不是显示器，因为尽管它是基于 ESP32 开发板，但他编写软件的目的是尽可能独立于平台和显示器。为了证明这一点，他把它制作成桌面应用程序和独立硬件。一个简单的图形用户界面允许选择一系列可用的源进行监控，图形结果显示在右侧。

该项目的所有代码和其他资产都可以在一个方便的 GitHub 库中找到[，为了测试它的速度，他甚至提供了一个视频，我们把它放在了 break 下面。连接 MQTT 的设备的用户界面既能听又能说，例如](https://github.com/rbaron/deskmate)[这个 MQTT 遥控器](https://hackaday.com/2019/12/26/handheld-mqtt-remote-for-home-automation/)。

 [https://www.youtube.com/embed/k03GiLAulfY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/k03GiLAulfY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

