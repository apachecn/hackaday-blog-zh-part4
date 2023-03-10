# 新零件日:内置神经网络的 RISC-V 芯片

> 原文：<https://hackaday.com/2018/10/08/new-part-day-the-risc-v-chip-with-built-in-neural-networks/>

有一天，在浏览了一些随机的网上商店后，[David](顺便说一句，谢谢你发来这篇文章)偶然发现了一个非常有趣的芯片。这是一个双核 RISC-V 芯片，运行频率为 400MHz。CPU 上有 6 MB 的 SRAM，还有 2MB 用于卷积神经网络加速。显然，有些版本有 WiFi。GitHub 上已经有 SDK 了，一个裸芯片也就一两块钱。感兴趣吗？登录淘宝，实现淘宝做预购，[而这一切都可以是你的](https://item.taobao.com/item.htm?&id=578484113485)。

这是一个预购订单，因为显然你可以在淘宝上作为一个卖家这样做，但 Sipeed M1 K210 是一个“核心”板，在一个 1 英寸的方形封装中有 72 个引脚，一个带 WiFi 的版本，或者是一个完整的开发板，带 OV2640 摄像头，2.4 英寸 LCD，麦克风和板载 USB。有这个芯片运行面部检测程序的视频。它找到了奥巴马。

谷歌搜索告诉我们，这款芯片来自[一家名为 Kendryte](https://kendryte.com/) 的公司，这里重复了规格:这是一款双核 RISC-V，带有一个 FPU 和一堆 RAM，可以运行 TensorFlow。[文档可用](https://kendryte.com/downloads/)，尽管[数据表将需要翻译](https://kendryte.com/downloads/)，并且在撰写本文时[有一个 GitHub，其中充满了 SDK](https://github.com/kendryte)和示例，一些回复在最后一个小时更新。

这些年来，我们已经看到了一些 RISC-V 芯片给开发板，你现在就可以买到。HiFive 1 是一款异常强大的微控制器，其处理能力足以与 Teensy(围绕飞思卡尔芯片构建)相媲美，但它也相当昂贵。我们不确定 [Arduino Cinque](https://hackaday.com/2017/05/20/arduino-cinque-the-risc-v-esp32-wifi-bluetooth-arduino/) (也是 RISC-V)是否已经投入生产，但是同样昂贵。RISC-V 微控制器只需几美元就能买到的想法非常有趣，它甚至附带了[SDK 和实用程序](https://github.com/kendryte)来使芯片变得有用。