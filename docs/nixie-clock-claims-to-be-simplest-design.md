# 谢妮时钟声称是最简单的设计

> 原文：<https://hackaday.com/2020/02/14/nixie-clock-claims-to-be-simplest-design/>

[Engineer2you]建造了一个[数码管时钟](https://www.youtube.com/watch?v=Xid7gH96P8I&feature=emb_logo)，并声称这是最简单的设计。我们觉得这是一个挑战。在这种设计中，电子管设置成矩阵，每行和每列都有光隔离器。矩阵有 60 个段，允许你用 16 位来控制它。有六列，每列对应一个数字。这意味着每行有 10 行。

Arduino 代码读取时钟，并以足够快的速度向电子管输出，以至于你的眼睛感觉到每个数字都是一直开着的，尽管它不是。

这可能是语义上的，但使设计简单的部分原因不是它本身简单，而是它确实使用了少量的密集模块。例如，时钟是 DS3231，有一个 DC 升压板为电子管产生 390V 电压。因此，这种设计不是最大限度地减少器件数量，而是通过采用包括 Arduino 在内的模块来最大限度地减少必须连接的器件数量。尽管如此，这还是有意义的。

看起来好像使用的谢妮管是苏联制造的。它们不需要超过 170 伏的电压就能点燃，至少需要 120 伏才能保持点燃。对于简单的直流-DC 转换器来说，这不成问题，因为电流非常低，约为 2.5 mA 左右。

我们假设有一天谢妮地铁的库存会消失。但是还是有[人在做](https://hackaday.com/2019/12/12/custom-nixies-perform-when-cranked-up-to-100000-hertz/)。或者你可以用[光导管](https://hackaday.com/2019/04/09/the-display-for-when-you-want-nixies-without-all-the-hassle/)做一个现代版。

 [https://www.youtube.com/embed/Xid7gH96P8I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Xid7gH96P8I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

