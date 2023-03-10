# 探索 90 年代早期另一个世界的视频游戏架构

> 原文：<https://hackaday.com/2020/01/17/exploring-early-90s-video-game-architecture-with-another-world/>

对过去的计算机架构很好奇？软件工程师【杨奇煜·桑格拉德】一直在尝试将动作冒险平台*另一个世界* 移植到不同的机器上，并在他的“另一个世界的多边形”项目中比较结果。

结果相当有趣。由于游戏基于多边形的图形，不同架构之间的优化差异很大，一些技巧允许软件在游戏发布前五年发布的硬件上运行。探索的游戏机主要来自 90 年代初，从 Amiga 500，Atari ST，IBM PC 和超级任天堂到世嘉创世纪。![](img/64d4af87c4d562206e5ac3c9573b0e15.png)

实际的游戏包含非常少的代码，原始版本有 6000 行汇编代码，而 PC DOS 可执行文件只包含 20 个 KiB。可执行文件只是作为一个虚拟机主机存在，它读取并执行 uint8_t 操作码，大部分业务逻辑用字节码实现。图形使用 16 种基于调色板的颜色，尽管 Amiga 500 支持多达 32 种颜色。然而，美学仍然很好地适合游戏，有一些非常令人愉快的像素艺术。

从最初的 Amiga 500 执行开始，每个端口中都出现了许多很酷的技巧。在 CPU/GPU 架构出现之前，微处理器具有位块传输器(blitters ),即快速修改内存中数据的逻辑块，能够与 CPU 并行复制大量数据，从而释放 CPU 进行其他操作。

![](img/94165076b731b793eb29e0b1c16dd7cd.png)

为了显示视觉效果，包含位图的帧缓冲区驱动显示器。使用了三个帧缓冲区，两个用于双缓冲，一个用于保存背景合成以避免重画静态多边形。在 framebuffer 中，有几个技巧用于改善图形体验。对于具有半透明色调的场景，通过“读取帧缓冲区索引，添加 0x8 并写回”从帧缓冲区索引中解释特殊值。

考虑到每台机器的 CPU 和总线带宽限制，在处理像素时也会遇到挑战。为了填充位，位阻击器使用一种称为“区域填充模式”的功能，从左到右扫描以找到边缘，用填充的行之间的空间来呈现位数组。由于帧缓冲区存储在五个独立的内存区域或位平面中，这需要绘制线条并填充区域四次，乘以引擎渲染的数百个多边形。解决方案是[建立一个临时的“暂存”缓冲区](https://scalibq.wordpress.com/2011/12/04/just-keeping-it-real-part-3/)并将一个多边形渲染到干净的空间。由于阻击器可以在内存的任何地方渲染，多边形可以通过屏蔽阻击操作复制到屏幕区域。

好奇吗？该系列继续深入探究雅达利街、T2、IBM 个人电脑和即将到来的 SEGA 创世纪/大驱动的报道。