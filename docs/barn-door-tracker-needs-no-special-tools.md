# 谷仓门跟踪器不需要特殊工具

> 原文：<https://hackaday.com/2019/05/10/barn-door-tracker-needs-no-special-tools/>

如果你想拍长时间曝光的照片，你需要一个三脚架来稳定你的相机。但是当它所站的地面移动时，三脚架就没用了。这正是[Emvilza]想拍摄几分钟或几小时的夜空照片时遇到的问题。他的解决方案是建造一个谷仓门跟踪器，他用英语和西班牙语仔细记录了这个跟踪器。

谷仓门跟踪器，也被称为苏格兰支架，多年来一直被摄影师用来抵消地球的自转。这使得星星看起来冻结在天空中，并允许拍摄非常暗淡的天体。这些追踪器的范围从[简单的手摇](https://hackaday.com/2016/12/15/build-this-barn-door-tracker-today-take-stunning-shots-of-the-galaxy-tonight/)事务到[复杂的机械创作](https://hackaday.com/2019/01/12/diy-guided-telescope-mount-tracks-like-a-barn-door/)。[Emvilza]决定尝试设计和制造自己的追踪器，只使用基本的工具，因为他没有 CNC 或 3D 打印机。

跟踪器本身是由木头制成的，带有金属硬件。[Emvilza]花了很多时间用 SketchUp 设计追踪器。精心制定的计划确保了一切都能够协调一致，正常运转。

最困难的部分之一是精确地弯曲螺纹杆，使其与跟踪器一起工作，但不束缚驱动系统。底座的运动来自一根螺纹杆。该杆由步进电机驱动。控制和感测由 ATmega328 处理，该 atmega 328 使用 Arduino 工具链编程。[Emvilza]学了 Eagle，设计了一个 PCB。他没有蚀刻电路板，而是简单地按照他的布局和走线在 perfboard 上构建电路。

最终的结果是一个外观和性能都很棒的追踪器——只需查看[Emvilza 的]网站上的[图片就可以看到一些例子。不仅如此，[Emvilza]写得很好的文档将帮助任何人在未来构建一个跟踪器！](https://sites.google.com/view/emvilza/proyectos/star-tracker/eng/photo-gallery)