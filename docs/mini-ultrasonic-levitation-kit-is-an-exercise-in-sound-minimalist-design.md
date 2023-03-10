# 迷你超声波悬浮套件是声音极简设计的一个练习

> 原文：<https://hackaday.com/2022/11/06/mini-ultrasonic-levitation-kit-is-an-exercise-in-sound-minimalist-design/>

对于那些没有听说过的人来说，超声波悬浮是一种过程，其中两个或更多的超声波换能器彼此相对设置，并以这样的方式激励，以便在它们之间产生驻波。顾名思义，这种声音是超声波——超出了人类的听觉范围——但又足够强，因此这些小而轻的物体可以被定位并固定在驻波压力最小的半空中。[Olimex]创造了一个小型的[超声波悬浮套件](https://olimex.wordpress.com/2022/10/12/ultrasound-levitation-soldering-kits-will-be-present-at-openfest-for-soldering-workshop/)来证明这一现象。

该套件本身是使用通孔组件制作的，以 ATTiny85 作为核心微控制器来驱动两个 TCT40-16T 超声波扬声器，以 MAX232 ~~提供 USB 接口~~来驱动换能器(感谢评论中的人进行更正)。两个开槽的矩形 PCB 片通过焊接连接到主板，提供了一个基座，以便设备在组装时可以直立。整个设备通过 USB 连接供电，超声波扬声器在 40 千赫范围内输出足够的功率来悬浮小聚苯乙烯泡沫球。

从设计上来说，这个项目是一个极简主义的实践，提供了一个易于组装的工具包，并提供了易于在设备上闪现、检查和修改的代码。所有的设计文件，包括材料清单、KiCAD 原理图和源代码都是在开源硬件许可下提供的，以允许任何想知道这样一个项目如何工作的人，或自己扩展它，有足够的机会。[Olimex]也有[套件出售](https://www.olimex.com/Products/Soldering-Kits/Ultra-Sound-Levitation/open-source-hardware)给那些不想自己采购电路板和零件的人。

我们以前展示过超声波悬浮装置，从 NE555 驱动的裸机系统到 T2 的大型相控阵。