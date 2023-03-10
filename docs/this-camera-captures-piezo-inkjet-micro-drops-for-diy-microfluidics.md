# 这款相机捕捉压电喷墨微滴，用于 DIY 微流体

> 原文：<https://hackaday.com/2020/04/15/this-camera-captures-piezo-inkjet-micro-drops-for-diy-microfluidics/>

在微流体学中，有“按需滴加”仪器来精确地沉积极小体积(皮升或纳升)的流体。这些设备非常昂贵，所以[Kyle]开始用业余爱好者级别的部件设计一个价格低于 1000 美元的系统。作为其中的一部分，他有一个特殊相机的迷人用例:[捕捉微滴形成时的形成和形状](http://www.kylescholz.com/wp/drop-observation-camera/)。

这项工作有许多不同的部分，值得一读，但两大设计元素归结为:

1.  使用压电元件制作微滴
2.  确保正确放置，并目视排除故障

[![](img/a0eed1c8f1e9a186868c30111e45cc36.png)](https://hackaday.com/wp-content/uploads/2020/04/Piezo-microdrop-camera-device.jpg)

Working prototype. The piezo tube is inside the blue piece at the top. The camera is to the right, and the LED strobe is on the left.

让打印机中的喷墨元件工作是一回事，但让压电元件以可控、可重复和可预测的方式分配任意液体则完全是另一回事。因为压电元件通过机械运动迫使液体流出，[不同的液体需要不同的驱动信号](http://www.kylescholz.com/wp/waveform-generator/)，这种实验需要一种方法来观察正在发生的情况，因此需要液滴观察相机。

[Kyle]最终从一个便宜的 USB 显微镜上取下镜头组件，用 3D 打印组件将其与他的 Korukesu C1 USB 相机相匹配。另一个 3D 打印外壳兼作灯箱，将压电管放在中心，LED 闪光灯和摄像头放在相对的两侧。整个集会有一些错误的开始，但最后[凯尔]似乎对他的结果很满意。[设备在这里简要描述一下高层次的](http://www.kylescholz.com/wp/diy-drop-on-demand-inkjet-platform/)。有一些粗糙的边缘，但它是一个工作系统。

喷墨技术已经存在很长一段时间了(你可以在这里看到一台使用了三十多年的喷墨打印机，但是值得一提的是，并不是所有的喷墨头都是一样的。大多数喷墨打印机头都是热运行的，这意味着一瞬间的热量会蒸发一些墨水来排出微滴。这些头不太适合微流体，因为它们不仅依赖于蒸发液体，而且除了它们设计的墨水之外，它们也不能很好地工作。压电打印头不太常见，但更适合[凯尔]正在做的工作。