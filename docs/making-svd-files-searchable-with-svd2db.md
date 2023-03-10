# 用 Svd2db 搜索 SVD 文件

> 原文：<https://hackaday.com/2022/11/21/making-svd-files-searchable-with-svd2db/>

每个为微控制器编写裸机代码的人可能都知道在参考手册中查找特定寄存器的详细信息的乐趣，包括它们的绝对地址。虽然 PDF viewer 的搜索功能很有帮助，但如果能够只搜索寄存器，并自动执行失调计算，那就更好了。这基本上就是[特里·波特]的 [Svd2db](https://mecrisp-stellaris-folkdoc.sourceforge.io/svd2db-v1.html) 工具所支持的。顾名思义，这个工具将基于 ARM 的 MCU 附带的 SVD 硬件描述文件转换为数据库文件。

这个数据库文件是一个 SQLite 数据库，允许使用提供的`readdb`工具或任何其他 SQLite 工具对其进行搜索。这将使该实用程序不仅对开发期间的快速查找有用，而且可能对自动化测试场景也有用，在这些场景中，拥有一个易于搜索的寄存器数据库是有用的。在这一点上，`Svd2db`保证可以与 STM32 SVDs 一起工作，但是也可以与其他基于 ARM 的 SVD 文件一起工作。