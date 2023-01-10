# DIY 掌上游戏把它的大脑放在一个可移动的推车上

> 原文：<https://hackaday.com/2021/08/16/diy-handheld-game-puts-its-brains-on-a-removable-cart/>

多年来，我们已经看到了大量的自制手持游戏系统，它们结合了一个 AVR 微控制器、几个按钮和一个小有机发光二极管显示器。其中一些甚至已经被转化为商业产品，比如 Arduboy。它们简单、便宜，并且有合适的软件，非常有趣。但是基于一个 MCU，他们中的大多数都有一个共同的限制，那就是在任何时候都只能玩一个游戏。

但不是游戏卡，由[迪伦特纳]。这款掌上电脑是专门设计的，这样游戏就可以很容易地用物理卡盒替换掉。但是，系统不是试图让系统的微控制器从外部闪存芯片引导代码，而是将微控制器重新定位到可移动的盒式磁盘上。这可能看起来有点大材小用，但考虑到每个墨盒上的 ATTINY84A 是多么便宜，它不会完全破产。

由于微控制器位于卡盒上，留在游戏卡上的唯一硬件是 SSD1306 128×64 有机发光二极管显示器、按钮和电池。这意味着手持设备实际上是不起作用的，除非有游戏插入，但这也可以说是最早期的基于盒式磁带的游戏系统。另一方面，它也为生产具有更强大微控制器的盒式磁带开辟了可能性。

为每个游戏使用不同的微控制器是一个巧妙的方法，但这不是问题的唯一解决方案。我们之前看到过[社区以 DIY 盒式磁带的形式为 Arduboy](https://hackaday.com/2019/06/07/the-arduboy-community-rolled-their-own-cartridge/) 添加可扩展存储的努力，这最终导致了[的开发，这是手持设备](https://hackaday.com/2021/03/04/arduboy-fx-mod-chip-now-youre-playing-with-power/)的官方闪存芯片升级。

 [https://www.youtube.com/embed/qE-Pg2zxOUw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qE-Pg2zxOUw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

