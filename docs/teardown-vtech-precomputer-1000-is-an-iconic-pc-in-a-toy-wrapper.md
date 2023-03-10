# 拆卸:伟易达预计算机 1000

> 原文：<https://hackaday.com/2019/11/19/teardown-vtech-precomputer-1000-is-an-iconic-pc-in-a-toy-wrapper/>

早在孩子们可以用 50 美元的安卓一次性手机安抚的日子里，许多年轻人被赠予一台所谓的“教育电脑”，让他们有事可做。这些小玩意总是看起来像他们父母不想让他们使用的真实电脑的狂热梦想版本，它们提供了单色的利用，使*佐克*看起来像*堡垒之夜*。同样由于其固有的硬件限制和作为教育玩具的前提，这些计算机上的“游戏”通常采取完成数学方程或回答历史问题的形式。

VTech PreComputer 1000 是这种特殊类型的教育玩具的完美典范。发布于 1988 年，它被宣传为一种让十多岁的孩子更容易操作真正的电脑的方法；从那时起，很明显，在未来的十年里，每个专业人士的桌上都会有一个米色的盒子。它的全尺寸 QWERTY 键盘在产品的附带资料中被特别提到，作为让年轻的手习惯触摸打字方式的一种方式。

[![](img/4baf9e68ca585c2cdb1dd945d5879e21.png)](https://hackaday.com/wp-content/uploads/2019/10/precomputer_manual.png)

Words of wisdom from the PreComputer 1000’s manual.

到 20 世纪 90 年代中期，这些设备已经取得了足够大的进步，可以包括尚可的文本到语音转换功能和原始图形，但初级专业人员发现自己坐在预计算机 1000 前时，得到的体验要简单得多。也许这种特殊的教育电脑被列为培训工具是件好事，因为即使在 1988 年，用这种玩具进行一次培训肯定感觉非常像工作。

但这并不是说预计算机 1000 没有自己独特的魅力。为了帮助巩固其作为更传统计算机的“培训师”的角色，VTech 认为给预计算机配备自己的 BASIC 解释器是合适的。它们甚至包括大量的书面文档，帮助年轻的程序员完成各种命令和功能。即使在今天，一个配有全键盘的移动设备也有一些奇怪的吸引力，它可以用电池运行基本程序超过 24 小时(即使它们是碱性“C”电池)。

让我们来看看这个有 30 多年历史的移动设备的内部，看看设计师们是如何设法以适合孩子的预算创建一个合理的实际计算的复制品的。

## 受到大师们的启发

如果预计算机 1000 的布局在现代人看来很奇怪，那只是因为我们已经习惯了现在无处不在的笔记本电脑外形。但标志性的翻盖设计对 1988 年的孩子来说并不意味着什么。东芝 T1100 被一些人认为是我们今天所知的第一台商用“笔记本电脑”，它仅在几年前发布，鉴于其高昂的价格，它不会成为一个常见的景象。

如果这个年轻人有任何使用电脑的第一手经验，那很可能是使用 Apple II、Commodore 64 或 TI-99 之类的产品。因此，PreComputer 1000 显然是对当时流行的“控制台”计算机的认可，可能不止是来自 TRS-80 Model 100 这样的便携式计算机的一点灵感。

但事实证明，与经典 8 位计算机的比较不仅仅是装饰性的。在检查 PreComputer 1000 的 PCB 时，我们可以看到它由一个 4 MHz Z80 处理器 Zilog Z84C0004PEC 驱动。

[![](img/e07ed497ef95876dc97e6f3bc4c0a289.png)](https://hackaday.com/wp-content/uploads/2019/10/precomputer_pcb_front.jpg)

还有一个现代 HY6116AP-10 提供 16K 内存和 1Mb VTech 品牌的 TC531000CP mask ROM，用于存储计算机的固件。相对稀疏的 PCB 周围点缀着各种支持 IC，如 74HC244AP 线路驱动器、HCF4011BE 与非门和 CD4508BE 4 位锁存器。

## 平淡无奇的输入输出

鉴于 PreComputer 1000 主板上的组件，可以有把握地说，这是一台与 20 世纪 70 年代末至 80 年代初的任何台式计算机一样真实的计算机。作为参考，1977 年推出的 TRS-80 I 型只有 1.4 兆赫的 Z80 处理器。

不幸的是，伟易达不得不在某些地方偷工减料，把价格降到玩具的水平。因此，虽然它可能拥有不到十年前的台式机处理器，但它配有相当糟糕的键盘和显示器。预计算机 1000 内部的 Z80 可能具有的任何潜力都被缓慢移动的辅助硬件严重阻碍了。

等待文本在 1×20 字符的小 LCD 上行进是非常糟糕的，但是，这些计算机上的显示器几乎总是很差。真正*让人*失望的是键盘。它可能有全尺寸 60%的布局，但不幸的是，这是我使用过的最糟糕、反应最迟钝的薄膜板之一。任何学会用这东西打字的人，当他们拿到一个合适的键盘时，一定会大吃一惊。

[![](img/b5608bce21ec32c3b607852ffe71d4f1.png)](https://hackaday.com/wp-content/uploads/2019/10/precomputer_keyboard.jpg)

## 扩展的可能性

像许多其他教育计算机一样，PreComputer 1000 具有一个扩展槽，可以接受能够增强系统基本能力的卡盒。在这样一个概念的早期例子中，这里的墨盒只是增加了系统可以向用户提出的问题的数量和种类，提供了诸如“超级科学”和“圣经知识”的标题。

 [![precomputer_cart1](img/6aa6d0940890bd2f2a573d100a6cca42.png "precomputer_cart1")](https://hackaday.com/2019/11/19/teardown-vtech-precomputer-1000-is-an-iconic-pc-in-a-toy-wrapper/precomputer_cart1/)  [![precomputer_cart2](img/300d1166cfe897beffcb16504a3b3df4.png "precomputer_cart2")](https://hackaday.com/2019/11/19/teardown-vtech-precomputer-1000-is-an-iconic-pc-in-a-toy-wrapper/precomputer_cart2/) 

这台电脑的拍卖包括一个“体育琐事”墨盒，在里面，我们可以看到除了几个无源器件和另一个 TC531000CP 掩模 ROM 外，板上什么也没有。有趣的是，这意味着每个扩展盒的存储容量与计算机本身一样大。至少在理论上，如果 VTech 愿意，这些盒式磁带似乎可以添加大量的软件。

正如我们在最近的项目[中所看到的，这些项目旨在扩展类似“玩具”计算机](https://hackaday.com/2019/10/14/repurposing-a-toy-computer-from-the-1990s/)的能力，如果社区中的任何人愿意，预计算机 1000 上的扩展端口可能有一天会得到更广泛的利用。虽然 LCD 仍将是一个绊脚石，但很难不好奇[将崩溃的 OS 卡盒](https://hackaday.com/2019/10/26/collapse-os-an-os-for-when-the-unthinkable-happens/)放入这台机器侧面的可能性。

## 一段历史

人们很容易将 VTech PreComputer 1000 视为简单的儿童玩具，但就其自身而言，它确实是一部合法的计算历史。凭借其正宗的 Zilog Z80 处理器、当代机箱设计和集成的 PRE-BASIC 解释器，该设备就像是 80 年代早期家庭计算的缩影。

经常阅读的读者可能会知道，这些每月拆卸的设备中的大多数最终都成为一堆有趣或有用的组件，用于一些未知的项目。但这一次，如此平淡的命运似乎有点不尊重人；正如亨瑞·琼斯博士曾经说过的，像这样的艺术品属于博物馆。

因此，预计算机 1000 将和我多年来收集的其他有趣的科技小摆设一起被束之高阁。但我也承认，在现代发明的帮助下，在稍加修补的情况下，我会在易贝再建一个，也许会获得新生。同时，我会给你一个简短的视频演示这个有趣的玩具变成的时间胶囊。

 [https://www.youtube.com/embed/_Wm8OtLWJys?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_Wm8OtLWJys?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

