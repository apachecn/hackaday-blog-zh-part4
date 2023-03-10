# 如果操作得当，控制器交换可以节省硬盘

> 原文：<https://hackaday.com/2021/12/11/controller-swaps-can-save-an-hdd-if-you-do-it-right/>

硬盘既脆弱又可靠。硬盘完全有可能出现故障，即使你的数据仍然完好无损地保存在里面的磁盘上。[Keith Sherry]最近试图从一个损坏的硬盘上为一个朋友恢复数据，并证明了现代的老把戏仍然可以工作。

有问题的驱动器是一个旧的 160GB 磁盘，它本身被用作备份。当然，一个你没有测试过的备份根本就不是备份，这个备份在最需要的时候失败了。

有人怀疑控制板是罪魁祸首，把控制板换出来可能会起死回生。过去，这是一种常见的黑客伎俩。然而，对于现代驱动器来说，它经常失败，因为现代驱动器在控制器板上存储了大量驱动器特定的校准数据。如果没有这些特定数据，另一个控制器将无法访问驱动器上的数据，甚至可能导致损坏。

然而，正如[Keith]所展示的，有一种方法可以解决这个问题。一个来自类似驱动器的控制器被采购，尽管来自驱动器的 SATA 版本而不是使用 USB 的原始版本。然后从原始控制器上取下一个芯片，其中包含该驱动器特有的校准数据。将这种芯片焊接到新的控制器上可以让一切正常运行，文件也可以恢复。

如果你的数据是非常宝贵的，那就很可能值得向专业人士付费。正如[Keith]所展示的，只要你的技术是最新的，旧的技巧仍然可以派上用场。狄莺你自己的数据恢复[可以做](https://hackaday.com/2019/12/24/hard-drive-data-recovery-why-not-diy/)，只是有风险而已。

哦，别忘了——一旦你恢复了文件，就把硬盘扔掉。不要一直用！休息后的视频。

 [https://www.youtube.com/embed/i2ihlSZh6xA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/i2ihlSZh6xA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢艾米的提示！]