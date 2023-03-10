# 新零件日:Alexa 连接套件现已发售

> 原文：<https://hackaday.com/2019/11/11/new-part-day-alexa-connect-kit-now-available-for-sale/>

订阅了 Alexa Connect Kit (ACK)更新的人最近会收到一封电子邮件，通知[该套件现已发售](https://www.amazon.com/dp/B07WJGSCH2/)。上一次[我们报道 ACK](https://hackaday.com/2018/09/20/new-part-day-put-an-alexa-in-everything/) 是在 2018 年 9 月,“发布”的绰号意味着“预览”,没有任何硬件可以实际购买。

一年多后，我们似乎终于可以把脏手套放在这个工具包上了，这应该能让我们的任何项目都支持 Alexa。这基本上似乎意味着，人们可以花近 200 美元从 [USI](https://www.usiglobal.com/) 购买一个 Arduino Zero 和一个 Arduino 盾装 WM-BN-MT-52 模块(虽然他们的网站上没有列出，但类似于 [WM-BN-BM-22](https://www.usiglobal.com/en/products?id=97bb6cc6-c459-424b-ad32-43cf1b54fc50#description) ？)集成了一个 192 MHz Cortex-M MCU 和一个 WiFi/蓝牙模块，正如亚马逊开发者页面为 ACK 总结的[。](https://developer.amazon.com/docs/ack/usi-dev-kit-overview.html)

## ACK 入门

该套件背后的想法是，使用 Arduino IDE 对基于 Cortex-M0+的 Arduino 板和应用固件进行编程。完全组装的套件将在网络上侦听来自 Alexa 应用程序(在智能手机或类似设备上)的任何[服务发现](https://developer.amazon.com/docs/device-apis/alexa-discovery.html#discover)广播，并根据[智能家居技能 API](https://developer.amazon.com/docs/smarthome/understand-the-smart-home-skill-api.html) 协议，以其能力的摘要来响应这样的广播。这本质上是 [mDNS 与 DNS-SD](https://en.wikipedia.org/wiki/Zero-configuration_networking) (服务发现)的应用。

当智能家居上的 Alexa 应用程序找到所有支持 Alexa 的设备后，你就可以使用 Alexa 语音界面来控制这些设备，例如打开和关闭它们，或者调整参数，如 PWM 控制的风扇的速度。亚马逊开发者网站为[提供了 Alexa 系统支持](https://developer.amazon.com/en-US/alexa/connected-devices/learn)哪种设备的概述，以供参考。

## 欢迎来到亚马逊围墙花园

对于那些已经冲出去得到 ACK 的人来说，他们将不幸地意识到 ACK 不仅仅是一个好玩的硬件。通过购买它，你实际上是签约成为亚马逊生态系统的一部分，从[注册亚马逊开发者账户](https://developer.amazon.com/docs/ack/dev-kit-set-up-environment.html)开始。正如[去年在 Register 的无畏记者](https://www.theregister.co.uk/2018/09/21/amazons_alexaonachip/)所指出的，ACK 的部分成本是你为使 ACK 工作的亚马逊云服务付费，亚马逊的 Alexa 服务器为你翻译客户的话语。

在撰写本文时，随 ACK 一起获得的 WiFi/蓝牙模块似乎也相当神秘，在互联网上没有数据表或详细信息。它似乎仅限于 802.11 b/g/n (2.4 GHz 单频带)WiFi，没有提到任何比蓝牙 4.1 支持更新的东西，这意味着它错过了蓝牙 5(和 BLE)的节能功能。

因此，一方面，有一件很酷的事情，通过一点 Arduino 争论和使用 Alexa Android 应用程序(或你客厅中的 Echo)，你可以制作你一直梦想的智能烤面包机，允许你通过简单的语音命令来烤面包机。另一方面，这意味着你完全依赖亚马逊的 Alexa 基础设施和 ACK 支持的继续存在。

## 我们以前来过这里

那些有几年物联网新闻的人可能会记得苹果的 [Homekit](https://en.wikipedia.org/wiki/HomeKit) ，从远处看，它至少看起来是 Alexa Connect Kit 的翻版，拥有苹果支持的硬件和 SDK，人们必须将它们集成到他们的产品中，才能实现智能家居的好处。 [Homekit 现在基本上依靠生命维持系统](https://www.theregister.co.uk/2018/08/09/apple_homekit/)。

![](img/f5ab1a5e2c20b44283def130e514d037.png)

Apple Homekit on iPad, iPhone and iWatch.

苹果去年决定放弃专利，转而加入由谷歌和 ARM 发起的线程组，专注于创建低功耗无线网络协议，适用于连接家庭内的智能设备。[线程](https://en.wikipedia.org/wiki/Thread_%28network_protocol%29)围绕 [IEEE 802.15.4](https://en.wikipedia.org/wiki/IEEE_802.15.4) 构建，IEEE 802.15.4 规定了一种低速率无线个人区域网(LR-WPAN)。同样的标准也是 Zigbee 的基础。支持该标准的网络是低功耗的，其特征数据速率为< 1 Mb。

当时持怀疑态度的观点是，ACK 提供的基于 WiFi 的家庭自动化正在击败同一匹死马，而苹果似乎一直在用 Homekit 击败它，只是用 Alexa 而不是 Siri。同样的怀疑者也可能会注意到，线程协议并不是一些人可能认为的开放和免费的灵丹妙药，一个人必须是线程组的(付费)成员，才能被允许对其开发进行任何输入，并被允许发布支持线程的设备。但是，如果你仍然渴望加入支持 Alexa 的潮流，并且能够忍受亚马逊规则的幽灵，那么大门现在已经打开了。