# TI-83 获得 CircuitPython 升级

> 原文：<https://hackaday.com/2019/04/04/ti83-gets-circuitpython-upgrade/>

图形计算器是一个有趣的利基市场。它们的功能相对较弱，通常配备廉价的低分辨率屏幕。它们之所以仍然可行，几乎完全是因为它们在教育中的应用，以及它们有限的连通性使它们适合在考试中使用。不过，这个市场开始升温了——TI 和 TI 最近在 TI-83 上用 Python 做了一些有趣的工作。

有传言说 TI 无法让 Python 直接在 TI-83 Premium CE 上运行。这导致了 TI-Python 外设的开发，它可以插入计算器的扩展端口。这允许用户用 Python 编程，TI-Python 完成工作，计算器本质上充当瘦客户机。里面的芯片是 Atmel SAMD21E18A-U，显然运行的是 Adafruit 的 CircuitPython 平台。

当然，这一发现导致了进一步的挖掘。经过一些黑客攻击，TI-Python 可以替换为基于 Atmel SAMD21 芯片的其他电路板。对于那些不在 Atmel 销售团队的人来说，这意味着当使用适当的 CircuitPython 固件进行闪存时，可以使用像 Adafruit 小饰品 M0 和 Arduino Zero 这样的东西来代替。这是一件棘手的事情，涉及到 USB IDs 和其他一些黑客技术，但没有什么是几个小时左右不能实现的。

这是早期的一次尝试，所以目前更多的是在这个阶段构建一个平台，而不是构建成熟的项目。当然，我们很期待看到 Twitter 客户端和多人游戏在不久后登陆 TI-83 平台。完成后，给我们一个举报热线的链接。

【感谢 PT 的提示！]