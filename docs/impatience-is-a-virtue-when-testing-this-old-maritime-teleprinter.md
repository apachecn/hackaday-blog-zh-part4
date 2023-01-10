# 测试这台老式海事电传打字机时，不耐烦是一种美德

> 原文：<https://hackaday.com/2022/07/16/impatience-is-a-virtue-when-testing-this-old-maritime-teleprinter/>

Perl 的发明者[拉里·沃尔]曾经说过一句名言，程序员有三个关键的美德:懒惰、傲慢和不耐烦。可以肯定地说，这些性格怪癖在某种程度上也存在于大多数硬件黑客身上，不耐烦可能是伟大黑客的主要驱动力。生命太短暂了，不能等待别人去创造它，不管它是什么。

当[黑掉一个 NAVTEX 接收器](https://baltic-lab.com/2022/07/sitor-b-navtex-test-signal-generation/)的时候，Sebastian (AI5GW)当然变得不耐烦了。NAVTEX 系统允许海上船只接收文本广播警报，例如天气变化或航行危险。问题是，每个 NAVTEX 电台每四个小时才传送一次，这使得电传打字机的测试不切实际。所以[Sebastian]的解决方案是创造他自己的 NAVTEX 发射机。

第一项工作是理解 NAVTEX 协议，这是一种 100 波特的 FSK 调制信号，其字符以 CCIR 476 编码。由于这种编码也用于业余无线电电传操作，[Sebastian]认为肯定会有一个 Arduino 库来编码和解码它。令人惊讶的是，原来没有，但是现在有了 T1，使得 Arduino 能够为 CCIR 476 编码的信息产生正确的脉冲序列。微型 NAVTEX 站的信号被输入一个函数发生器，很容易被速度慢得令人痛苦的电传打字机接收和记录下来。又是那种不耐烦。

我们认为这是一次巧妙的黑客攻击，我们特别感谢[Sebastian]的努力，他的成果是一个将来可能对 hams 和其他无线电爱好者有用的库。我们已经谈论了一些更现代的业余无线电数字模式，如 [WSPR](https://hackaday.com/2021/04/15/the-50-ham-a-simple-wspr-beacon/) 和 [FT8](https://hackaday.com/2021/02/10/the-50-ham-digital-modes-with-wsjt-x/) ，但也许是时候看看其他一些模式了。

 [https://www.youtube.com/embed/xW5NRssfzhk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xW5NRssfzhk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

