# 将图片刻录到 CD-R 上，不需要特殊的驱动器

> 原文：<https://hackaday.com/2022/07/11/burn-pictures-on-a-cd-r-no-special-drive-needed/>

当我们日常携带存储数十或数百千兆字节数据的设备时，有时会震惊地想起，曾经有一段时间，650 MB 的 CD 确实是一件大事。这些古老的存储介质最初是银色的预录制 CD-r om，后来成为可录制 CD-r。大多数人最终都拥有了 CD 刻录机，一些别致的刻录机具有在光盘未使用的部分蚀刻图片的功能。

没有漂亮的光驱，想要刻录机吗？[别担心，【arduinocelentano】有一个解决方案](https://hackaday.io/project/186303-burning-pictures-on-a-compact-disc-surface)，用软件为标准 CD 刻录机写入磁盘映像，刻录机的数据在光盘上形成可视映像。

CD-r 有一层薄薄的邻苯二甲酸染料夹在聚碳酸酯光盘和镀银漆层之间。它们通常是金色的，但镀银实际上只是铝。这些数据被编码成一系列的坑和脊，这些坑和脊是由激光蒸发一小部分染料来打孔的。

该代码创建了一个标准 CD-ROM 会话的数据结构，该数据结构不包含任何可用的数据，而是排列其凹坑和平台以形成图像。您可以在 GitHub 资源库中找到所有内容，并尝试创建自己的产品。我们本可以为我们的照片制作一个旋转光盘，但是对于我们中一些曾经深陷其中的人来说，很遗憾我们再也没有 CD-r 了。