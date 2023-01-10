# 这是你可以自己制作的延迟踏板

> 原文：<https://hackaday.com/2019/04/10/this-is-the-delay-pedal-you-can-build-yourself/>

如果你想在电子行业赚钱，没有比吉他踏板和模块化合成器更好的市场了。利润率很高，所有的消费者都是宅男，他们会花惊人的钱追逐下一件大事。这些产品比零氧气电缆的高保真手淫只差一步，如果你的运算放大器听起来“更透明”，你将会大赚一笔，不管某些东西听起来如何更透明，不管那是什么开始。

如果你想做一些真正酷的事情，建立一个延迟，因为每个人都需要另一个延迟。如果你想建立最新的延迟技术，只需抓住一个 PT2399 芯片。这就是 electro mash[用他们的开源时间操纵器 delay](https://www.electrosmash.com/time-manipulator) 所做的。一切都在那里，所有的电路部分都有描述，你也可以成为一名效果踏板工程师。

这个踏板基于普林斯顿技术公司的 PT2399 芯片，这是一种数字延迟芯片，可以与听起来像老派水桶大队芯片或类似磁带回声的东西一起使用。作为一个数字芯片，只需稍微调整一下电路，你就能获得干净、清晰的数字延迟声音。在之前，我们已经看过 PT2399，但令人惊讶的是，没有多少人分享他们的秘密。

用于 ElectroSmash 时间操纵器的电路围绕 ATMega328 构建，该芯片与 Arduino Uno 中的芯片相同，具有两个 PT2399s，可以配置为串行或并行操作，用于从冲击回波到 600ms 数字延迟的各种操作。如果你把一切设置正确，你可以得到合唱，混响，或一些心理法兰样的声音。

整个电路是开放的，有一个用 KiCad 设计的电路板，代码就在那里用 C 编写，唯一难以复制的技术是 PT2399 芯片本身，它可以从通常的供应商那里以不到一美元一个的价格买到。这是一个伟大的踏板，一定要看看下面的视频。

 [https://www.youtube.com/embed/bbDv9qQvuLQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bbDv9qQvuLQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

