# 长达一年的有机发光二极管老化实验

> 原文：<https://hackaday.com/2019/04/23/a-year-long-experiment-in-oled-burn-in/>

如果你需要给你的项目添加一个小显示器，你不会比一个小小的有机发光二极管显示器做得更好。这些微型显示器是黑白的，通常分辨率为 128×64 或其他可被 2 整除的数值，它们在 I2C 上空行驶，图书馆很容易得到，而且很便宜。在显示一些数字和文本方面，你不可能比 much 有机发光二极管做得更好了。不过，有一个问题:OLEDs 会烧坏，或者烧坏，这取决于你如何定义它。这些 OLEDs 的寿命有多长？[这正是【聚焦电子】正在测试的](https://www.youtube.com/watch?v=GWOFF5tMv_A) (YouTube，俄语，点击隐藏字幕按钮)。

实验装置是 11 台 128×64 像素的有机发光二极管显示器，配有 SSD1306 控制器，全部由 I2C 的 STM32 驱动。一切都在试验板上，实际显示是 16 个街区，每个街区一个接一个地点亮，中间有一秒钟的显示。这是为了测试逐渐增加的烧毁程度，从表面水平分析，这是一个很好的方法来看看有机发光二极管像素是否烧毁。

经过 378 天的测试，在没有失败的显示后，该测试被停止。这有一个警告:在一年的耐久性测试后，有一些像素烧毁。与这些像素打开的频率相关联。解决这个问题的方法是偶尔“晃动”屏幕上显示的文本，在没人看的时候关掉显示器，或者为 OLEDs 编写一个屏幕保护程序。最后一点已经做到了，这里有会飞的烤面包机来证明。这是一个有趣的实验，虽然你正在做的那个奇怪的项目可能不会让平安有机发光二极管持续运营一年，但它仍然值得思考。下面视频。

 [https://www.youtube.com/embed/GWOFF5tMv_A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GWOFF5tMv_A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

