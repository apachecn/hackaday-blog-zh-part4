# 脚踏板提升 Vim 生产率，带来人体工程学优势

> 原文：<https://hackaday.com/2022/12/16/foot-pedal-ups-vim-productivity-brings-ergonomic-benefits/>

Vim 是有史以来最伟大或最糟糕的文本编辑器，这取决于你所在的部落。无论哪种方式，两个阵营的成员都可以欣赏[Chris Price]，[的这种构建，它使用脚踏板来简化用户的操作。](https://blog.scottlogic.com/2022/12/08/building-a-rusty-vim-clutch.html)

基本概念是使用踏板来实现正常模式和插入模式之间的切换。在 Vim 的前身 vi 中，切换模式很容易，ESC 键就在 ADM-3A 终端键盘上的 Q 旁边。然而，在现代键盘上，这是一种痛苦，因此脚踏板是一种理想的解决方案。在 Vim 领域，它被称为“Vim 离合器”

该建筑使用了来自易贝的廉价踏板开关，其中安装了一个树莓派 Pico。Pico 连接到开关触点，并被编程为 USB HID 设备。当踩下踏板时，Pico 发送一个“I”键进入 Vim 的插入模式。释放踏板会让 Pico 发送一个“ESC”键返回正常模式。

那些经常使用 Vim 的人可能会喜欢这种设备带来的生产力提升。此外，还有一些人体工程学的好处，不必紧张一个人的手来达到 ESC 键。当然，[这是一个老派的解决方案](https://hackaday.com/2012/06/21/building-a-clutch-for-vim/)，但仍然有一些令人信服的和下一级的东西关于一个脚踏板连接到一个人的开发装备。