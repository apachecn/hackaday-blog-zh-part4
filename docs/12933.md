# 得益于光纤，大 LED 矩阵变成了小 LED 矩阵

> 原文：<https://hackaday.com/2022/03/01/big-led-matrix-becomes-tiny-led-matrix-thanks-to-fiber-optics/>

每个人都喜欢 LED 矩阵，即使你在商业上找不到你喜欢的，也很容易做出你想要的。需要大的吗？没问题；点个大 PCB 和几个 WS2812s 就行了。需要小东西吗？有可笑的小 led 将测试你的 SMD 技能，以及你的视力。

但是如果你想要一个实际上是大矩阵伪装的小矩阵呢？为此，你应该效仿[elliotmaded]的做法，将光纤融入你的 LED 矩阵。构建从 WS2812B 可寻址 led 的 16×16 矩阵开始，间距相当小，但边长仍为 160 mm。柔性矩阵夹在金属背板和塑料挡板之间，每个 LED 正上方有孔。每个孔接受 1.5 毫米长的柔性丙烯酸光管材料的一端；另一端插入一块 35×7 的类似孔的铝块中。这个小块由支架支撑在基板上方，但看起来好像优雅的纤维束支撑着较小的显示器。

运行 CircutPython 程序的 Raspberry Pi Pico 完成了控制 led 的工作，正如你在下面的视频中看到的，效果非常可爱。当小型显示器工作时，从光纤中漏出的光正好能在背景中制造出一场迷人的表演。我们已经看到了这种东西的一些实际用途，但我们认为这只是漂亮而已。不过，它确实给了我们在电路雕塑中加入光纤的想法。

 [https://www.youtube.com/embed/e9nGw1BpO-Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/e9nGw1BpO-Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

