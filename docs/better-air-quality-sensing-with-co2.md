# 利用 CO2 实现更好的空气质量检测

> 原文：<https://hackaday.com/2022/11/21/better-air-quality-sensing-with-co2/>

任何试图解决这个问题的人都可以证明，测量空气质量并不像看起来那么简单。即使模糊的术语“质量”被定义了，大多数传感器还是用某种东西来代表整体的空气健康状况。一种常见的方法是使用挥发性有机化合物(VOCs)作为这种替代物，但正如拉里·班克(Larry Bank)发现的那样，在一个有功能厨房的家里使用这些会导致很多不准确的读数。为了寻找更可靠的传感器，他建立了这个项目，利用二氧化碳来帮助测量空气质量。

二氧化碳传感器不被用作空气质量传感器的主要原因是成本。它们比 VOC 传感器贵得多，但[Larry]最近发现了一种更实惠的传感器，并决定围绕它开展这个项目。原型使用 Arduino 通过 I2C 与传感器和有机发光二极管屏幕进行通信，他最终将它放在 3D 打印的盒子中，以便随身携带，在不同的现实世界位置采样二氧化碳浓度。最终的项目使用了一种[巧妙的方式与我们之前展示的电子纸显示器](https://hackaday.com/2022/11/21/driving-e-paper-displays-with-memory-limited-mcus/)互动。

虽然二氧化碳浓度并不能说明某个特定地方空气质量的全部情况，但它确实起着重要作用。[Larry]在他家里发现浓度高达 3000 ppm，这可能导致认知功能下降。他改变了一些生活方式，据他报告，这产生了有益的影响。对于人类居住的室内空间，二氧化碳很容易成为空气质量差的主要原因，我们已经看到至少[另一个项目直接解决这一问题](https://hackaday.com/2022/10/07/ceiling-fan-adds-co2-sensor/)。