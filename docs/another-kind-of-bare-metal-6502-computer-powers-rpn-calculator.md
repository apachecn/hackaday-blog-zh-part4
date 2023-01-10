# 另一种“裸机”:6502 电脑电源 RPN 计算器

> 原文：<https://hackaday.com/2020/11/17/another-kind-of-bare-metal-6502-computer-powers-rpn-calculator/>

[Mitsuru Yamada]指出,[这款 6502 电脑的目标之一是让它足够坚固，能够在现实世界中使用。就这一点而言，我们称之为成功；使用的压铸铝外壳是过去的一个小爆炸，并为项目增添了一个漂亮的复古工业外观。电脑的主机箱上布满了发光二极管和厚重的拨动开关，用于设置数据和地址总线。内部同样整洁，6502 微处理器(1995 年的日期代码)和相关的支持芯片整齐地排列在 perf 板上。施工方法是电线包裹，以保持老派的外观和感觉。甚至手绘的示意图也是一件艺术品——有点像](https://hackaday.io/project/175866-6502-standalone-computer)[【福里斯特·米姆斯】](https://hackaday.com/2017/01/18/forrest-mims-radio-shack-and-the-notebooks-that-launched-a-thousand-careers/)。

至于编程，这机器低得不能再低了。这里只有 6502 机器语言，用拨动开关手动输入，或通过外部编程的 ROM 输入。这台机器只能寻址 1k 的内存，这是支持 RPN 计算器插件的代码也遇到的限制，为 992 字节。计算器键盘有一个 20 键矩阵键盘和一个 8 位点阵 LED 显示屏，可以对定点二进制编码的十进制输入进行四种基本操作。下面的简短视频展示了计算器的运行。

我们喜欢这个建筑的外观，我们渴望看到更多这样的建筑。我们最近已经看到了大量由分立芯片构建的 [6502，虽然我们也喜欢这些，但很高兴看到一个大的旧 dip 重新开始改变。](https://hackaday.com/2019/04/04/a-6502-computer-with-acres-of-breadboard-and-dozens-of-chips/)

 [https://www.youtube.com/embed/vmzrgA2PHII?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vmzrgA2PHII?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

