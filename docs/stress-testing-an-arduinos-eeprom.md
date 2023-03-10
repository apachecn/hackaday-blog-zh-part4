# 对 Arduino 的 EEPROM 进行压力测试

> 原文：<https://hackaday.com/2022/04/07/stress-testing-an-arduinos-eeprom/>

每当我们中的一个人闪现 Arduino 的内部存储器时，我们脑海中挥之不去的想法提醒我们，尽管生活中的一切都是短暂的，但非易失性可重写存储器更是暂时的。在任何 EEPROM 模块出现故障之前，写入次数都是固定的，那么每次上传出错代码时，我们是否都在浪费写入次数？简而言之，我们大多数人都不应该真的关心这个问题，除非我们像[AnotherMaker]所做的那样继续写数据，直到 Arduino 中的内存最终失效。

这方面的软件相当简单。他简单地将前 256 个`int`全写为 0，读取它们以确保它们都在那里，然后用 1 重复这个过程。在大约一个月的时间里，他连续迭代了数百万次，终于得到了他的第一次读取失败。超过这一点的进一步写入只会加速内存模块的死亡。通过这种方法，他能够在设备出现故障之前获得近 300 万次写入，这远远超过了此类设备通常估计的数万次或数十万次写入。

为了证明这不是一个异常值，[AnotherMaker]重复了这个测试，并在写入更少的内存时做了一些其他的测试。有了这个，他能够将周期数提高到 500 万以上。假设 Arduino Nano 克隆没有使用令人惊讶的高质量 EEPROM，我们可以安全地假设我们大多数人没有什么可担心的，我们的 Arduino 将在未来几十年内发挥作用。[除非一个坏的 Windows 驱动不小心砖了你的设备](https://hackaday.com/2015/02/08/unbricking-a-counterfeit-ftdi-chip/)。

 [https://www.youtube.com/embed/McK2PSUxjck?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/McK2PSUxjck?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[摩根]的提示！