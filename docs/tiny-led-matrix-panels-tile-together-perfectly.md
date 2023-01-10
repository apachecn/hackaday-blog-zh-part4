# 微小的 LED 矩阵面板完美地拼接在一起

> 原文：<https://hackaday.com/2022/01/06/tiny-led-matrix-panels-tile-together-perfectly/>

LED 矩阵项目有很多值得赞赏的地方，它们往往看起来很酷。但是他们中的大多数依赖于来自过剩市场的 RGB 矩阵面板，虽然这没有什么错，但构建自己的[微小、可平铺的 LED 矩阵面板](https://hackaday.io/project/183387-tileable-tiny-8x8-sk6805-rgb-matrix)使这些构建稍微酷一点。

这些矩阵面板有很多值得赞赏的地方，尤其是它们无缝拼接的方式。但是为了达到那个目的，[sjm4306]有很多准备工作要做。他从一个简单得多的 5×7 阵列开始，在定制的 PCB 上使用流行的 WS2812 RGB LEDs。经过一点实践，是时候转向更小的 SK6805 LEDs 了，它们以 8×8 矩阵的形式排列。电路板布局尽可能紧凑；[sjm4306]报告称，这将 PCB 工厂推向了极限，但他最终在电路板上实现了 led 的完美间距，并且当电路板彼此相邻时，有足够的余量来保持二维空间的一致间距。

至少可以说，组装电路板是一项挑战。下面的视频显示，该设计几乎没有留下足够的空间来用镊子处理 led，并且需要一些花哨的技巧来将电路板放在热板上或从热板上取下以进行回流。[sjm4306]表示，他将在未来探索 JLC PCB 的组装服务，因为每块电路板的组装都需要一个小时。但当它们用菊花链连接在一起时，看起来棒极了，接缝处没有可察觉的缝隙。

有了这样的矩阵，可能性是无限的。我们甚至在 Hackaday.io 上发布了一份 LED 矩阵项目的完整列表供您查看。

 [https://www.youtube.com/embed/e6PX6aNmWsg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/e6PX6aNmWsg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

