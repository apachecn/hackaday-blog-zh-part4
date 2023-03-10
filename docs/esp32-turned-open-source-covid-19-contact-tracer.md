# ESP32 转向开源新冠肺炎接触跟踪

> 原文：<https://hackaday.com/2020/07/28/esp32-turned-open-source-covid-19-contact-tracer/>

在过去的几个月里，我们听到了很多关于接触跟踪器的消息，这种跟踪器旨在通知用户他们是否可能与病毒携带者有过密切接触。一般来说，这些系统都是基于智能手机应用程序的，但也有一些硬件解决方案可以为那些不能或不愿意安装软件的人独立运行。这正是[【汤姆·本斯基】使用 ESP32 和 USB 电池组](https://github.com/tbensky/npct)实现的。

想法很简单:软件生成一个唯一的 ID，由 ESP32 通过蓝牙低能量广播出去。附加到该 ID 上的是一个代码，表示该人当前的身体状况。没有集中的数据库，每个用户都需要每天更新他们的设备，以了解他们可能遇到的任何症状。如果你的追踪器在闪烁，这意味着有人已经足够接近了，你应该看看收集的数据，看看他们当时的感觉。

当然，这并不是一个完美的系统，首先，愿意并能够将这个固件刷新到备用的 ESP32 上并整天随身携带的人会非常少。如果我们今年夏天还会去参加黑客和制造商大会，这可能会填补一个有趣的空白，[但所有这些都已经虚拟化了](https://hackaday.com/2020/07/21/stay-at-home-hope-and-def-con-will-come-to-you/)。也就是说，这是一个有趣的视角，可以看到一个分散的联系人追踪系统是如何廉价而快速地实现的。

另一个值得关注的细节是[Tom]如何在他的固件中处理用户体验。为了让追踪器尽可能容易配置，他使用了谷歌 Chrome 的网络蓝牙功能。只需在浏览器中打开本地网页，它就会为您处理与硬件的对话。即使您不想购买合同追踪器，我们也认为这是如何在 ESP32 上处理最终用户配置的绝佳范例。

我们已经关注了来自谷歌和苹果的联系追踪 API，专用的新冠肺炎硬件令牌，甚至其他开源的分散邻近追踪的尝试。需要处理的事情很多，每个人似乎都有自己的想法。最后，最实际的解决办法可能就是尽可能呆在家里。