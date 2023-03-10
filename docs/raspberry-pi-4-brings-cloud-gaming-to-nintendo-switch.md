# 树莓 Pi 4 将云游戏带入任天堂 Switch

> 原文：<https://hackaday.com/2021/01/05/raspberry-pi-4-brings-cloud-gaming-to-nintendo-switch/>

谷歌(Google)和微软(Microsoft)等公司一直在大力投资云游戏的概念，玩家使用自己的电脑或移动设备来传输游戏的视频，游戏运行在隐藏在某个数据中心的强大机器上。有了这项技术，即使你使用的设备没有本地运行的处理能力，你也可以播放最新最棒的游戏。

考虑到 Switch 已经是一个便携式系统，任天堂似乎对这项技术不感兴趣也就不足为奇了。但是这并没有阻止斯坦·德米特列夫自己做一些实验。除了一个树莓 Pi 4 和小饰品 M0，他还展示了用户可以远程与交换机互动，足以实时玩游戏。

[![](img/dd395ad4a8c5fdb523badca45fb54512.png)](https://hackaday.com/wp-content/uploads/2020/12/switchstream_detail.jpg) 设置相当简单。一个[廉价的 HDMI 捕获设备](https://hackaday.com/2020/12/21/heavy-raspberry-pi-user-keep-an-hdmi-to-usb-capture-device-around/)被用来从任天堂 Switch 码头抓取视频，然后在 Pi 的硬件视频编码器的帮助下被流式传输到网络上。用户的输入通过 Pi 的 UART 发送到小饰品，而小饰品本身[运行一个专门为模仿任天堂 Switch 控制器而开发的固件](https://github.com/gdsports/NSGadget_Pi)。由于涉及到如此多的元素，自然会出现一些延迟。[Stan]报告的大约 100 毫秒的延迟对于快节奏的游戏来说并不理想，但对于更轻松的游戏来说绝对足够了。

在软件方面，该项目使用的是由[Stan]的雇主 SurrogateTV 开发的[SDK。如果你想让你的游戏或其他互动小工具上这项服务，现在你需要申请，尽管他说这项服务将于明年向公众开放。但是，即使没有所有的细节，我们也清楚地知道视频捕捉和用户输入这两方面是如何处理的。对于个人使用，您真正需要做的是构建一个简单的 web 界面，将所有这些联系在一起。](https://docs-beta.surrogate.tv/)

这不是我们第一次看到用[微控制器与开关](https://hackaday.com/2017/10/25/teensy-script-plays-nintendo-switch-strikes-out/)接口。其他游戏机在与什么样的硬件对话方面更有选择性，但[微软自适应控制器可能允许你在 Xbox 上做类似的事情](https://hackaday.com/2018/05/17/open-gaming-to-everyone-with-a-controller-meant-to-be-hacked/)。