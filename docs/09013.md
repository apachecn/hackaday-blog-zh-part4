# 留意热水器指示灯

> 原文：<https://hackaday.com/2021/01/21/keeping-an-eye-on-the-water-heater-pilot-light/>

[WJCarpenter]的燃气热水器使用一个小指示灯，需要持续点亮，以根据需要点燃主燃烧器。一年四五次，指示灯熄灭，需要手动点亮。这包括一次从楼上浴室到地下室的探险，总是在清晨，在等了几分钟热水之后。厌倦了这种练习，[WJCarpenter]建造了 [Water Watcher](https://hackaday.io/project/176690-the-water-watcher) ，这是一个带有一些 esp 和一个光传感器的指示灯监控系统。

Water Watcher 由一个 ESP8266 组成，它连接到一个贴在热水器观察窗上的光传感器上。它通过 [MQTT](https://hackaday.com/2019/07/25/mqtt-deep-dive/) 向主卧室中基于 ESP32 的 M5 原子矩阵报告指示灯的状态，主卧室使用 5×5 RGB 矩阵显示指示灯状态，如休息后所示。两个 esp 都运行 [ESPHome](https://hackaday.com/2020/04/20/roll-your-own-automation-with-esphome/) ，所以编程就像给它一个 YAML 配置文件一样简单。[WJCarpenter]测试了几种不同的光传感器，直到他发现了 TSL2591，它对正确的波长敏感，并且具有足够的动态范围来观看指示灯。

这可能不是一个复杂的技巧，但我们不怀疑它在那些灾难性的早晨减少了一点沮丧。一定要看看水观察者项目网页，这是一个有趣的阅读！

 [https://www.youtube.com/embed/PYlJUFb8QNI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PYlJUFb8QNI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

