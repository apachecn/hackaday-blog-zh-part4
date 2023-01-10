# RCA Plug 独自演奏 16 分钟的 Chiptune 乐曲

> 原文：<https://hackaday.com/2021/05/05/rca-plug-plays-sixteen-minute-chiptune-piece-all-by-itself/>

在电子游戏的黄金时代，街机的常客可能会回忆起从一个完整的街机传来的混合声音，那种你把你的硬币堆在一台机器上，声称自己是下一个玩游戏的人。它们是喧闹的地方，充满了简单但引人注目的声音，伴随着磷光体和硅的魔力在四周展开。

这种简单配乐的日子可能已经一去不复返了，但他们肯定不会被忘记，这款内置在 RCA 插头中的 chiptunes 发生器既是对这种风格的致敬，也是优化和小型化的绝佳例子。这是[girst]的作品，它的出现是为了尝试在硬件中实现[Rob Miles]'[C 小调的位移变体](http://txti.es/bitshiftvariationsincminor)算法生成的 chiptunes 作曲。在第一次尝试中，[girst]选择了 ATtiny4 作为微控制器，将它和低通滤波器所需的 SMD 元件放在一个柔性 PCB 上，并将整个东西包裹在一个纽扣电池周围。发电机被塞进 RCA 插头的外壳中，当它被插入音频输入插孔时会进行检测，并开始播放 16 分钟的音乐。[girst]还制作了第二个版本，使用了红木 PSM150c [“三分微控制器”](https://hackaday.com/2019/09/09/everything-you-wanted-to-know-about-padauk-mcus-and-more/)芯片。

这是芯片调谐最小化方面的一大成就。我们已经看到了 32 字节的芯片调谐(T1)、T2 的 Altoids tin 芯片调谐(T3)以及邮票大小的 PCB 上的 EP(T5)，但这一款可能会在尺寸上击败它们。

 [https://www.youtube.com/embed/uld88xn8JPA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uld88xn8JPA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

