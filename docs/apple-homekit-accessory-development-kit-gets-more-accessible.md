# 苹果 HomeKit 配件开发包变得更容易使用

> 原文：<https://hackaday.com/2019/12/27/apple-homekit-accessory-development-kit-gets-more-accessible/>

每个技术垄断者都有自己专有的智能家居标准；锁定你的客户比在他们的家中建造一个特定的解决方案更好吗？在这些参与者中，苹果传统上被认为是最神秘的，这一称号是它凭借几十年的封闭标准和专有解决方案赢得的。当谈到他们的智能家居小工具连接解决方案 HomeKit 时，这种声誉越来越不值得。2017 年，他们向前迈出了一大步，不再需要单独的认证芯片来与 HomeKit 交互。上周，他们又做了一次，并且[也发布了他们的 HomeKit 配件开发套件(ADK)](https://github.com/apple/HomeKitADK) 的一大块。如果你很惊讶没有早点听到消息，那可能是因为它结合了关于苹果、亚马逊、Zigbee 联盟的更大消息，以及更多关于[更开放、可互操作的家庭物联网标准](https://www.connectedhomeip.com/)的合作。回到 2030 年，看看这是如何形成的。

> “HomeKit ADK 实现了 HomeKit 附件协议(HAP)的关键组件，体现了苹果为智能家居技术带来的核心原则:安全性、隐私性和可靠性。”
> –自述文件中的一个描述性宝石

苹果之前的放松限制允许人们开始制造可以与他们的 iOS 设备自然交互的设备，而不需要特定的苹果出售的“认证芯片”来认证他们。这意味着现有的商业设备可以成为支持 OTA 的 HomeKit，并且[的爱好者可以以认可的、非黑客的方式互动](https://hackaday.com/2019/07/14/homekit-compatible-sonoff-firmware-without-a-bridge/)。其中一部分是(非商业) [HomeKit 规范本身的发布，可以在这里](https://developer.apple.com/homekit/specification/)获得(有苹果开发者登录和许可协议)。

尽管在新闻稿中有许多令人屏息的提及，但很难说 ADK *实际上是什么。README 和文档目录中没有答案，但是通过对 GitHub repo 的其余部分的研究给了我们一个思路。它由两个主要部分组成， [HomeKit 附件协议](https://github.com/apple/HomeKitADK/tree/master/HAP)本身和[平台抽象层](https://github.com/apple/HomeKitADK/tree/master/PAL)。HAP 实现了 HomeKit 本身，PAL 是一个包装器，可以让你把它插入到一个新的系统中。这是一个相当有内容的软件；HAP 的主标题长达 4500 行，不需要太多搜索就能找到一些[令人恐惧的 50 行预处理宏](https://github.com/apple/HomeKitADK/blob/master/HAP/HAPTLV.c#L340)。这是一个很好的开始，但坦率地说，我们认为要让所有人都能访问 ADK，还需要更多的文档。*

如果不是显而易见的话，上面的大多数工具都经过了苹果公司的仔细许可，并且是用于非商业用途的。虽然我们非常感谢有机会得到这样的接口，但我们确信许多人会对这是否真的算“开源”吹毛求疵([它被授权为 Apache 2.0](https://github.com/apple/HomeKitADK/blob/master/LICENSE.md) )。我们会在评论中留给你。