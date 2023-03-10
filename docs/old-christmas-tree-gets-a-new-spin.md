# 旧圣诞树有了新的旋转

> 原文：<https://hackaday.com/2019/12/15/old-christmas-tree-gets-a-new-spin/>

几年前的圣诞节，[Nick]厌倦了试图均匀地装饰他的巨型假树，他做了一个 MDF 旋转木马，让它像蛋奶酒一样简单。但是如果树的一边总是对着墙，那么平衡的装饰又有什么意义呢？今年，[尼克]给了自己一个新项目的礼物，将“懒苏珊”机动化，让树慢慢旋转。

圣徒[尼克]决定完全从垃圾箱里拿出来做这件事，除了所有的 WS2811 RGB 发光二极管，他希望与树的运动同步。他首先在 OpenSCAD 中设计了一个齿轮，以适应轴承的外径，由于开源齿轮库的出现，这项任务变得更加简单。

他手头的 NEMA-23 很难实现缓慢平稳的运动，但他没有放弃，而是买了一个不同的马达，设计了一个齿轮系统让它工作。我们最喜欢的部分是由唱机连接器制成的 DIY 滑环(Nick ),以解决给旋转的东西供电的问题。这是一项正在进行的工作，所以还没有视频。你可以观看[【尼克】的推特](https://twitter.com/nickzoic/)更新。

[Nick]没有具体说明他为什么选择使用 WS2811s，但它们已经变得非常便宜。你知道吗[你可以用 VGA](https://hackaday.com/2016/01/04/driving-ws2811-leds-with-vga/) 驱动它们？

Via [Adafruit 的 CircuitPython 简讯](https://blog.adafruit.com/2019/12/11/icymi-circuitpython-newsletter-200-circuitpython-libraries-binho-ble-and-more-python-adafruit-circuitpython-icymi-circuitpython-micropython-thepsf-adafruit/)