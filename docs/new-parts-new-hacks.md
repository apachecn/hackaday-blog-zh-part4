# 新零件，新技术

> 原文：<https://hackaday.com/2021/01/23/new-parts-new-hacks/>

本周最大的新闻是，Raspberry Pi 不再是单板 Linux 计算机的同义词:他们的第一个芯片 RP2040 和支持分线板 Pico 正在涉足微控制器业务。这是一款价格实惠、功能强大的微控制器，由一家以前从未生产过微控制器的公司生产，所以这很新鲜。

黑客们对这款芯片的评论如火如荼，一些评论者哀叹板载无线电台的缺乏。我猜这是一个半满的玻璃杯，但 RP2040 *不是*ESP32，伙计们。是别的东西。它的袖子里藏着一个真正让我着迷的硬件——可编程输入/输出(PIO)单元。

和我一样，另一半评论者对尝试一些新功能垂涎三尺。当然，PIO 在这个列表中名列前茅，但这个芯片也迎合了那些做高速 DSP 的人，快速乘法例程烧入 ROM 和一个不错的累加器。(当你通读一份 663 页的数据手册，并思考所有可以使用和/或滥用硬件外设的有趣方式时，你就知道自己是一个微控制器呆子。)

所有的芯片设计都是妥协。没有什么可以做一切。新的外围设备，旧元素的新颖组合，以及令人愉快的设计决策，如果你愿意寻找它们，就会带来新的机会。当 ESP32 是新的时候，我看着他们古怪的并行 I2S 硬件，想着那会实现什么样的疯狂黑客，而[聪明的黑客](https://hackaday.com/2019/03/07/esp32-drives-controllerless-display-using-i2s-hack/)已经[证明我是对的](https://hackaday.com/2019/02/05/back-to-video-basics-with-an-esp32-vga-display/)。我敢打赌 PIO 也是类似的。

新芯片为黑客开辟了新的可能性。你打算拿他们怎么办？

This article is part of the Hackaday.com newsletter, delivered every seven days for each of the last 200+ weeks. It also includes our favorite articles from the last seven days that you can see on [the web version of the newsletter](https://mailchi.mp/hackaday.com/hackaday-newsletter-649368). Want this type of article to hit your inbox every Friday morning? [You should sign up](http://eepurl.com/gTMxQf)!