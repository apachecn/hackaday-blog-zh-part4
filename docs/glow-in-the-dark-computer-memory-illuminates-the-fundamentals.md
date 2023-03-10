# 黑暗中发光的电脑存储器照亮了基本面

> 原文：<https://hackaday.com/2022/04/11/glow-in-the-dark-computer-memory-illuminates-the-fundamentals/>

这些年来，计算机存储器有了多种形式，从水银延迟线管到手工编织的磁芯。如今，使用半导体的易失性存储在计算中已经变得无处不在，但如果有更好的方法呢？[迈克尔·科恩]一直在研究一种新的计算机内存标准，这种标准使用在黑暗中发光的标签。

显然我们是在开玩笑，但是我们仍然被这个演示深深打动了。八个令人愉快的星形磷光贴纸代表八位内存，总共一个字节。深色材料中的辉光粘在短圆柱体的内部，每个圆柱体包含一个白色 LED 和一个光电晶体管。内存阵列连接到 iceFUN FPGA 板，然后通过电平转换器连接到西方设计中心 MENSCH 单板计算机。

使用 6502/65C816 汇编语言将“1”写入存储器就像写入相应的存储器地址一样简单。使用 STA 命令将点亮该存储地址处的白色 LED，进而使黑暗标签发光并“保存”状态。相反，同一地址的 LDA 将从光电晶体管中读取，光电晶体管会拾取标签发出的光(或无光)。

当磷光消失时，需要刷新周期来维持存储器阵列上的 0 和 1，这与需要频繁充电来维持存储器内容的现代 DRAM 没有什么不同。整个设置是易失性计算机内存基础的有形演示，将成为一个有趣的初学者项目。[迈克尔]在他的[网站](https://www.mikekohn.net/micro/glow_in_the_dark_memory.php)和 [GitHub](https://github.com/mikeakohn/glow_memory) 页面上有更多细节。

虽然 FPGA 板有自己的一组闪光灯，但一个 8 位 RGB LED 阵列会让这个项目更加明亮。

 [https://www.youtube.com/embed/4QUYWIOCYHQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4QUYWIOCYHQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

