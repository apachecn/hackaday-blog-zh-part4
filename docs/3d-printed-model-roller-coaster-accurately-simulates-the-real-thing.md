# 3D 打印模型过山车精确模拟真实的东西

> 原文：<https://hackaday.com/2021/12/30/3d-printed-model-roller-coaster-accurately-simulates-the-real-thing/>

虽然模型过山车没有真实过山车那样的刺激感，但观看起来总是很有趣。然而，它们实际上是全尺寸乘坐的糟糕模拟，因为重力和空气阻力不会以相同的方式缩小，模型过山车通常比现实世界中相同设计的过山车移动得更快。[Jon Mendenhall]通过设计一个精确模拟全尺寸乘坐的模型过山车解决了这一缺陷。

轨道和手推车都是由 3D 打印件制成的，总共花费了大约 400 个小时来打印。该系统独特运动的主要技巧是推车是电动的:无刷 DC 电机使用齿条齿轮系统沿轨道移动它。这意味着，从技术上来说，这个模型不是过山车，因为手推车从来没有重力驱动下降；它实际上是一个小型铁路，由车上携带的锂离子电池供电。ESP32 驱动电机，通过 WiFi 接收其命令，而完整的设置由 Raspberry Pi 控制，它通过预定的序列运行小车。

轨道的设计灵感来自于 [Fury 325](https://en.wikipedia.org/wiki/Fury_325) 过山车，并在 [NoLimits 2](https://nolimitscoaster.com/) 中模拟。[Jon]编写了自己的软件，根据模拟器的输出生成所有要打印的内容。这包括所有的轨道部件以及支撑它们的大型 A 形框架；其中一些太长，不适合[Jon]的 3D 打印机，必须用更小的部件来建造。物理模拟还以脚本的形式向控制器提供输入，该脚本包含轨道上每一点的适当速度和加速度。

与其他模型过山车相比，最终结果看起来相当慢，但如果你想象自己在车里，实际上会感觉很真实。虽然它不是我们见过的第一个 [3D 打印过山车](https://hackaday.com/2021/07/23/3d-printed-roller-coaster-looks-pretty-darn-fun/)，但它可能是唯一一个精确模拟真实事物的过山车。如果你对过山车的安全系统更感兴趣，[我们也特别介绍了它们](https://hackaday.com/2021/12/02/the-safest-model-roller-coaster/)。

 [https://www.youtube.com/embed/jkkf6wcAqkc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jkkf6wcAqkc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

