# 制造 IOT 车库门开门器的考验和磨难

> 原文：<https://hackaday.com/2019/07/15/the-trials-and-tribulations-of-building-an-iot-garage-door-opener/>

车库门可能是令人沮丧的事情，手动打开是一件苦差事。许多人选择安装电动开启器，但对一些人来说，这还不够。将车库门连接到物联网长期以来一直是一个受欢迎的项目，[西蒙·卢德博尔兹]决定尝试一下。当然，一路上会有一些障碍需要克服。

[西蒙]的构建相对简单，使用 ESP-12 作为操作的大脑，通过 WiFi 连接到互联网。然而，健壮性是该项目的主要目标，依赖不稳定的云服务是不行的。这款开启器也设置为独立于互联网连接工作。除了网络上提供的网页外，还有一个漂亮的控制面板，上面有发光的按钮来操作开启器。

在开发过程中，[西蒙]遇到了几个障碍。[一组卷帘门电机被意外损坏](http://ludzinc.blogspot.com/2019/07/my-garage-door-opener-hardware.html)，并且在让网页界面正常工作时出现了[问题。](http://ludzinc.blogspot.com/2019/07/my-garage-door-opener-software.html)然而，这些都不是引人注目的东西，经过一点点工作和一些新的部件，一切最终都走到了一起。该项目随后获得了一个适当的商业级案例，来自阿里巴巴。对于一个有望持续使用多年的项目来说，这是一个很大的进步。他还花时间记录了[他为更简单的 ESP8266 开发](http://ludzinc.blogspot.com/2019/07/easier-esp8266-development.html)提供的技巧，这可能对那些刚刚开始使用该平台的人有用。

车库开门器仍然是这里的一个常见主题，但每个项目都有自己的故事要讲。如果你已经为你的车库出入问题开发了一个特别独特的解决方案，[你知道该找谁。](http://hackaday.com/submit-a-tip)