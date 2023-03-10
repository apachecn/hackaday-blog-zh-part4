# 用于家庭自动化的手持式 MQTT 遥控器

> 原文：<https://hackaday.com/2019/12/26/handheld-mqtt-remote-for-home-automation/>

如果您正在从事一个家庭自动化项目，那么您现在可能已经深深地陷入了 MQTT。如果不是，你应该是。轻量级消息协议是在互联网上获取“东西”的理想选择，通过简单的 web 界面或移动设备上的应用程序就可以轻松控制它们。或者如果你是[serverframework]，[你给自己做了一个帅气的小一体化 MQTT 遥控器](https://pseudo-server.com/blog/wi-fi-remote-using-an-esp8266/)。

[![](img/93b05073fd701675879203d03a7a0e37.png)](https://hackaday.com/wp-content/uploads/2019/12/mqremote_detail.jpg) 这里的硬件相当简单；内部只有一个 NodeMCU ESP8266 开发板，一些按钮，一个 RGB LED 以提供反馈，以及一个 3.7v 1200mAh LiPo 电池和相关的充电模块。所有东西都放在一个漂亮的小木箱里，看起来很适合客厅的装饰。我们希望在组装电路的裸露电路板上有某种盖子，但这可能是个人偏好。

这个项目中的大部分魔法实际上都发生在软件方面。所提供的源代码不仅可以处理与 Home Assistant 的所有 MQTT 通信，而且它还提供了一个聪明的用户界面，允许[serverframework]只需五个按钮就可以执行 25 个功能。不，你没看见什么。该设备上实际上有六个按钮，但其中一个是专用的“电源”按钮，可以将遥控器从深度睡眠中唤醒。

如果您想更多地了解如何让这个协议为您服务，我们的常驻 MQTT 专家[埃利奥特·威廉姆斯]在这个问题上有很多想法。从[他在 2017 年 Hackaday super co](https://hackaday.com/2019/11/07/found-footage-elliot-williams-talks-nexus-technologies/)的演讲到[他的家庭自动化教程系列](https://hackaday.com/2016/05/09/minimal-mqtt-building-a-broker/)，有大量的信息让你开始。

 [https://www.youtube.com/embed/DNxjFqAbx98?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DNxjFqAbx98?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

