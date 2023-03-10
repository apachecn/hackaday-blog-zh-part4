# CircuitPython 滑入第 100 块板——OHS 2020 徽章

> 原文：<https://hackaday.com/2020/01/21/circuitpython-slithers-into-100th-board-the-ohs-2020-badge/>

CircuitPython 上周迎来了一个重要的里程碑，迎来了它的第 100 块电路板:[手表形状的徽章](https://hackaday.io/project/168483-open-hardware-summit-2020-badge)是为[第 10 届年度开源硬件峰会](https://2020.oshwa.org/)设计的，该峰会将于 3 月 13 日在纽约举行。尽管 circuit python——MicroPython 的开源衍生产品——诞生于 Adafruit，但这个列表中超过一半的电路板都是在公司外部生产的。这正好显示了社区支持蛇的力量。

OSHW 2020 徽章加入了一系列熟悉的板，很高兴把你放进 Python 解释器。其中有 Adafruit Feather 生态系统，ItsyBitsy，专门的电路板，如 Supercon 的一些礼品袋中的 Edge Badge，以及 circuit playground——现在有蓝牙版本的瑞士军刀传感器。第一批 100 个主板以强劲的势头完成了【乔伊·卡斯蒂略】的 [OpenBook 电子阅读器](https://hackaday.com/2019/10/31/building-an-open-hardware-ebook-reader/)和 [Teensy 4.0](https://hackaday.com/2020/01/14/circuitpython-now-working-on-teensy-4-0/) 。

## 看着 OSHW 的未来开始

~~[![](img/589cdb77582ef593b4bd42c6e202887a.png)](https://hackaday.com/wp-content/uploads/2020/01/OSHW-2020-inset.png) 如果你在 2019 年 Supercon 展会上遇到了德鲁·富斯蒂尼，你很有可能会看到这个令人敬畏的腕表徽章的原型，因为它正在被传来传去。~~这一设计的灵感之一是来自[2019 cc camp 的 card10 徽章，这是一款双 PCB 腕表外形](https://hackaday.com/2019/08/29/hands-on-cccamp2019-badge-is-a-sensor-playground-not-to-be-mistaken-for-a-watch/)。

OHS 板基于 Rigado BMD340 模块内的 Nordic nRF52840。它有很多功能，包括环境传感器、手势传感器和 9 自由度 IMU。为了给你一些尺度，前面是一个 1.54 英寸的液晶显示器。还有一个内置的 LiPo 充电器和一个 Sparkfun QWIIC 连接器，可以通过 IC 轻松连接其他传感器、继电器等。

根据 IO 页面，这个项目仍然欢迎贡献者和评论，因为该板仍在开发中。不幸的是，对我们许多人来说，徽章不会出售，但每个参加 2020 年 OSHW 峰会的人都会得到一个这样的美女。另一方面，该项目的开源特性意味着如果你真的想要一个，你可以自己组装。

## CircuitPython 对微控制器项目的影响

CircuitPython 的易用性使其成为适合所有年龄段初学者的良好平台。游戏总是学习任何东西的有趣方式，如果你是 CircuitPython 的新手，[de∫hipu]的 [PewPew Standalone](https://hackaday.io/project/159733-pewpew-standalone) 将为游戏编程提供一个学习环境。来自“闭嘴，拿走我的钱”部门的 CircuitPython 负责人 [Scott Shawcroft](https://twitter.com/tannewt) 正在为[的 CircuitPython](https://circuitpython.org/board/gb_m4/) 开发一款兼容游戏机的卡带。斯科特在 2019 年 Supercon 2019 上发表了关于这个主题的演讲，我们将在未来几周内重点介绍这个主题。

CircuitPython 是 MicroPython 的一个分支，它是基于 C 构建的。CircuitPython 通过将 Python 解析为字节代码来工作，这使得它在两端都很强大——增强了程序员的能力，他们不必学习 C，同时利用 C 的处理能力。这也意味着您可以从一种芯片架构转移到下一种架构，而不必重新学习每个特定系统的所有基础。

对于每个人来说都有一些小东西，所以如果 CircuitPython 还没有蜿蜒到您的工作台，请查看官方支持的板列表。