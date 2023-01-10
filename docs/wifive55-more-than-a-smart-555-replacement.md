# WiFive55:不仅仅是智能 555 的替代品

> 原文：<https://hackaday.com/2021/04/15/wifive55-more-than-a-smart-555-replacement/>

"你可以用一个 555 定时器做到这一点."但是如果你手头只有一台 ESP8266 呢？[TechColab]需要通过固态继电器(SSR)用短脉冲控制电磁阀，但发现可靠的 555 定时器很难正确设置。此外，他们希望增加一些难以实现的功能，如固定脉冲长度，即使使用多个定时器也是如此。仍然希望保持东西便宜和容易获得，[TechColab]创造了[wifi ve 55，这是基于 ESP-01 ESP8266 板的 555 替代品。](https://hackaday.io/project/178964-wifive55)

[TechColab]从调查现有的 ESP-01 固态继电器板开始，但发现[许多继电器板在启动时会立即启用输出](https://hackaday.com/2017/09/26/an-introduction-to-solid-state-relays/)——这种风险[TechColab]认为是不可接受的。这一问题在 WiFive55 中得以解决，方法是在 SSR 输出端添加一个 RC 滤波器，消除输出毛刺，代价是将开关时间降至 20 ms 左右，这对许多 SSR 应用来说是可以接受的。

由于他们打算设计一种新的 PCB 来支持这种改进的 ESP-01 SSR 控制器，[TechColab]决定全力以赴。为了支持各种不同大小的负载，PCB 支持开关电流最高达 1 A 的光隔离器、开关电流最高达 2 A 的 MOSFET 以及开关电流最高达 3 A 的片上继电器或 SSR，对于重负载，它包括片外 SSR 的连接，允许它切换 SSR 能够处理的任何电流(轻松超过 50 A)。由于 ESP-01 的功能比 555 稍强，因此 WiFi 55 支持通过 WiFi、GPIO、串行和按钮进行控制。与 WiFive55 作为 555 替代品的原始角色保持一致，它甚至包括一个暴露类似 555 的触发器和输出接口的标题！

我们总是喜欢看到像 ESP-01 这样的廉价电路板被充分利用，我们迫不及待地想看看[TechColab]为此开发了什么软件！如果你对开始使用 ESP-01 感兴趣，你可以考虑从[这份通过 WiFi 闪烁 LED 的指南开始。](https://hackaday.com/2019/02/26/blink-an-led-on-the-internet-of-things/)