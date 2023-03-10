# ExpressLRS:开源、低延迟、远程 RC 协议

> 原文：<https://hackaday.com/2021/01/19/expresslrs-open-source-low-latency-long-range-rc-protocol/>

遥控飞行爱好的新手必须做出的一个主要选择是遥控链路协议。为了增加选择(或混淆)的列表，现在有一个新的开源、低延迟、远程协议，名为 [ExpressLRS](https://github.com/AlessandroAU/ExpressLRS) 。

ExpressLRS 的名声在于高达 500 Hz 的高分组速率，计划为 1000 Hz，以及低至 5 ms 的[延迟](https://hackaday.com/2018/02/26/quantifying-latency-in-cheap-rc-transmitters/)，远程测试已经用飞翼将其推出 30 公里(下面的视频)，但这对于其他协议来说并非闻所未闻。大多数现代 RC 协议运行在 2.4 GHz 或 915/868 MHz 频段，后者在范围方面具有明显优势。

ExpressLRS 可以选择在任一频段上运行，使用 Semtech SX127x (915/868 MHz)或 SX1280 (2.4 GHz) [LoRa](https://hackaday.com/2020/01/28/rf-modulation-crash-course-for-hackers/) 收发器，连接到 STM32、ESP32 或 ESP8285 微控制器。ESP 微控制器还允许通过 Wi-Fi 进行软件更新。

我们很高兴看到目前主导市场的专有协议的开源竞争对手，但几年来几个开源协议来了又走。硬件可用性和兼容性是新协议成功的决定性因素，ExpressLRS 在这方面已经具有优势。现有的 Frsky R9 发射器和接收器以及浸入式 RC Ghost 接收器与固件兼容。也有 DIY 选项可用，GitHub 页面声称有几家制造商正在开发官方的 ExpressLRS 硬件。

如果你已经对 RC 感兴趣，并且有兼容的硬件，一定要试一试，并给开发者一些反馈！我们希望看到测试的一个场景是高干扰和拥挤的频带条件，如遥控飞行活动。

所有的源代码和硬件设计都可以在 GitHub 上找到，在 [Discord](https://discord.gg/dS6ReFY) 上也有活跃的社区讨论。

 [https://www.youtube.com/embed/SbWvFIpVkto?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SbWvFIpVkto?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢提示[Jye]！