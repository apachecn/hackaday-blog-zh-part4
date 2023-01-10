# 了解每一个细节 13

> 原文：<https://hackaday.com/2019/06/02/getting-to-know-every-bit-of-an-attiny13/>

我们最近听说一个黑客在一个 8 位微控制器上实现了一个特别好的 VGA 黑客:“他个人知道所有的位。”好评，确实。如果你想对一大堆晶体管直呼其名，那就看看[海因茨 D]在 ATtiny13 汇编器中的[假期课程(原文为德语，](http://www.elektronik-labor.de/AVR/KursAssembler/T13asm13.html)[在这里被机器人翻译成英语](https://translate.google.com/translate?sl=auto&tl=en&js=y&prev=_t&hl=en&ie=UTF-8&u=http://www.elektronik-labor.de/AVR/KursAssembler/T13asm13.html&edit-text=&act=url))。

但是要注意，这不是学习 AVR 的简单方法。这个长达一个月的 AVR 汇编“课程”并不满足于简单地剥离每一层抽象，它开始用高电压和低电压的本地机器语言对芯片进行编程。但是，特别是如果你能一次完成几项任务，你就可以用汇编语言写得相当精彩，并且很快就可以用一个合适的程序员上传代码，因为在发疯之前，一个人能输入多少代码是有实际限制的。

这种完全自下而上的方法有一种美丽的极简主义，也许这是一个学习机器如何在其最底层工作的合适起点。无论如何，你都可以对 Arduino 团队称王称霸，因为你只需要一对机械触点和一块电池就可以让它正常运行。[真正的程序员](https://www.xkcd.com/378/) …

一旦你掌握了 AVR 汇编语言，你可以回收这两个按钮来[学习 I2C](https://hackaday.com/2013/08/11/bitbanging-i2c-by-hand/) 或 SPI。还有哪些协议没有禁止超时？你一点一点输入过最疯狂的代码是什么？