# 给你的 FPGA 增加一点苏联时代的超级计算能力

> 原文：<https://hackaday.com/2019/05/03/add-a-bit-of-soviet-era-super-computing-to-your-fpga/>

MESM-6 项目致力于将 20 世纪 60 年代的苏联 BESM-6 计算机带入现代的 FPGAs 和 HDL 时代。目前，这项保护工作背后的团队由[【叶夫根尼·哈卢耶夫】](https://twitter.com/x86128)【塞尔日·瓦库伦科】和【利奥·布鲁希斯】组成，他们负责俄语[项目页面](http://www.besm6.org/)的工作。

BESM-6 (俄语:бэсм-6，“bolshaya elektronno-schetnaya mashina”或“大型电子计算机”)是一台高性能的苏联超级计算机，于 1968 年首次推出，并在接下来的 19 年中一直在生产。它的系统时钟运行在 9 MHz，使用了数量惊人的分立元件，如 60，000 个晶体管和 170，000 个二极管，总共能够寻址 192 kB 的内存。在建造的 355 座中，有几座幸存至今，其中一座在伦敦科学博物馆展出(见上图)。更多的图片和信息可以在它的[俄语维基百科页面](https://ru.wikipedia.org/wiki/%D0%91%D0%AD%D0%A1%D0%9C-6)上找到。

对于那些没有俄语知识的人来说，[机器翻译的摘要](https://translate.google.com/translate?hl=en&sl=ru&tl=en&u=https%3A%2F%2Fgithub.com%2Fbesm6%2Fmesm6%2Fwiki)揭示了项目的目标是在 SystemVerilog 中制作一个与用户模式 BESM-6 兼容的软核，使用与该系统最初使用的相同的 Pascal 编译器。进一步的目标包括至少 24 kB 的数据存储器、96 kB 的命令存储器，以及增加 SPI 和 I2C 等现代外设。

该系统旨在与 Arduino IDE 集成，使用 Pascal 编译器使任何有兴趣对这样的系统进行编程的人都可以高度访问它。考虑到该项目的麻省理工学院许可证，人们可以想象在未来的 FPGA 工作中使用一点苏联时代的计算能力。

如果在看完 BESM-6 的视频后——包含在下面——你觉得有灵感开始你自己的苏联计算项目，我们想用俄罗斯的方式祝你好运:нипуханипеиа！

> 通过 becm-6 测试(2008 年记录)。T0 https://t . co/SVF 1 hevuof t1 和 T2 pic . Twitter . com。
> 
> —x 86128(@ x 86128)[2018 年 4 月 18 日](https://twitter.com/x86128/status/986431756889874433?ref_src=twsrc%5Etfw)