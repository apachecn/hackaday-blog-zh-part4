# 64 位和显示器:十年后的《我的世界》计算机

> 原文：<https://hackaday.com/2020/06/06/64-bit-and-a-display-minecraft-computers-10-years-later/>

有的人自建电脑玩游戏，有的人玩游戏自建电脑。《我的世界》是后者的主要候选人，虽然你当然可以安排这些模块使它们看起来像计算机，但我们当然是在谈论复制 CPU 或其部件的实际功能，和/或游戏中的外部组件。自从第一个《我的世界》制造的 ALU 浮出水面以来的十年里，许多这样的创造已经诞生了，并且[Rockfarmor]制造了一个 64 位样本来添加到那个列表中——[，并且制作了一个视频来展示它](https://www.youtube.com/watch?v=A_EStNvK2MQ)。

[Rockfarmor]没有模仿一个普通的建筑，而是采用了一种更加自制的方法，并重新使用了旧学校作业(瑞典语)中的建筑作为基础。结果是一个简单但功能齐全的 64 位 CPU，具有 32 个寄存器、32kB 主内存和一个独立的 16kB 堆栈。指令集主要包含 ALU 和分支操作，但也有一些特殊的操作码来控制额外的 64×64 ~~像素~~块，64 色显示——包括绘制圆形、线条和颜色填充。

关于这个架构的更多细节可以在[它的文档](https://docs.google.com/document/d/1NfDmDYPnpaJvmY7EqdSZpa3C7JCXjeHkXDTkb1w0dow/)和[一个更老的视频](https://www.youtube.com/watch?v=gCAQdrBz04o)中找到(不幸的是音频环境很差)。一个额外的[初始建造](https://www.youtube.com/watch?v=LdxXk6xDTXE)的延时视频也是可用的，休息后你会发现它们全部。为了简化开发，[Rockfarmor]还编写了一个桌面应用程序，用汇编语言给电脑编程，然后直接上传到《我的世界》版本。

和所有《我的世界》制造的电脑一样，驱动力是 [*红石*](https://minecraft.gamepedia.com/Tutorials/Redstone_computers) ，本质上允许[在游戏内进行电路设计](https://minecraft.gamepedia.com/Mechanics/Redstone/Logic_circuit)，【Rockfarmor】的在这里没有区别。他还使用[命令块](https://minecraft.gamepedia.com/Tutorials/Command_blocks_and_functions)来避免否则所需的费力而缓慢的“布线”，使其更像一个“无线红石”电路。

毫无疑问，纯粹主义者会认为这是作弊，但从另一个角度来看，考虑到计算机的大小和速度与第一个《我的世界》算术逻辑单元相比，它可以被视为摩尔定律应用于《我的世界》计算机。或者作为真实世界 CPU 中的微码的等价物？或者，也许我们应该接受和拥抱不同的选择和偏好。

 [https://www.youtube.com/embed/A_EStNvK2MQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/A_EStNvK2MQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent) 
 [https://www.youtube.com/embed/gCAQdrBz04o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gCAQdrBz04o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent) 
 [https://www.youtube.com/embed/LdxXk6xDTXE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LdxXk6xDTXE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)