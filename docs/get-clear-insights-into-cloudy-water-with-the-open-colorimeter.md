# 使用开放式比色计，清晰观察混浊的水

> 原文：<https://hackaday.com/2022/10/24/get-clear-insights-into-cloudy-water-with-the-open-colorimeter/>

化学和生物学的基本科学工具是比色计设备，用于测量特定样品溶液吸收的光的波长。色度计的一些应用是测量 pH 值或氯含量，测量污染物，如油或农药，在某些情况下，甚至可以用于测量 RNA/DNA 浓度。甚至今天的大多数洗衣机都有专门的色度计传感器，用来测量浊度(混浊度)以提供清洁过程的反馈。为了帮助建立你的家庭科学实验室，[IORodeo]发布了一款[开放式色度计](https://blog.iorodeo.com/cuvette-holder-design/)。

![A blown out diagram of the Open Colorimeter showing the 3d enclosure, the PyBadge, the LED board and sensor along with text describing each element](img/e6d4a92324183d40a7a156e094d82c0e.png)

开放式比色计是一个独立的设备，可接受装满液体的[比色皿](https://en.wikipedia.org/wiki/Cuvette)进行测试。基本结构是一个安装在电路板上的 LED，它透过充满样品的比色皿，然后在另一端由 TSL2591 颜色传感器进行测量。开放式比色计具有独立的专用 LED 板，波长范围从 470 纳米到 630 纳米，并集成了一个 PyBadge，用作主微控制器以及显示和输入。

[IORodeo]对该设备的组装、使用和测试做了大量的[文档记录](https://blog.iorodeo.com/open-colorimeter/)。他们还提供了测量氨、硝酸盐、亚硝酸盐和磷酸盐的[协议](https://blog.iorodeo.com/ammonia-api-colorimetric-assay/)，此外还提供了许多其他物质的吸收谱资源。所有与 [3D 外壳](https://github.com/iorodeo/colorimeter_enclosure)、[固件源代码](https://github.com/iorodeo/open_colorimeter_firmware)、[原理图和 Gerbers](https://github.com/iorodeo/basic_led) 相关的文件都在开源硬件兼容许可下提供。对于那些不想自己建造的人，[IORodeo]正在出售他们的 T10。

这不是我们第一次展示色度计，一些人制作了一个 DIY 版本，另一些人在 T2 的三录仪项目中使用它。开放式色度计是对这个列表的一个很好的补充，并且已经为黑客攻击和扩展做好了准备！