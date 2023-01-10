# 竖起大拇指为这个自定义雅达利 5200 控制器

> 原文：<https://hackaday.com/2018/08/08/thumbs-up-for-this-custom-atari-5200-controller/>

它可能已经近 40 岁了，但雅达利 5200 仍然激励着大批粉丝重温他们年轻时的 8 位辉煌岁月。游戏控制台有很多可爱之处，但操纵杆和键盘控制器并不在其众多魅力之列。操纵杆不能自动居中，按钮软绵绵的，人机工程学也不存在。

不过，复古爱好者不必默默忍受，这要感谢 Atari 5200 的这款替代控制器。[斯科特·贝克]不想满足于一个商业替代品，或者，恐怖的是，一个老式 PC 风格操纵杆的适配器，所以他推出了自己的产品。根据 Atari 的原始原理图，[Scott]设计了一个计划，使用一个现成的拇指控制器作为他的构建基础。关键问题是如何使新操纵杆上的 10k pots 适应预期 500k pots 的环境，他使用模拟到数字再回到模拟的方法解决了这个问题。ATtiny85 上的 ADC 将每个操纵杆电位计的电压转换为 0 至 255 之间的数字值，然后发送至 100K 数字电位计。稍微摆弄一下 RC 常量就可以使它回到控制台所期望的状态。拇指棒和按钮安装在定制的 PCB 上——感谢[Scott]设计了一个双手灵巧的电路板。下面的视频展示了实际的设计和成品。

[斯科特]这些天有点 5200 踢；他刚刚为这款古老的游戏机完成了一个树莓派多弹药筒。他的控制器应该能让游戏机上的复古游戏更容易上手。

 [https://www.youtube.com/embed/IST-PSk7r-A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IST-PSk7r-A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

