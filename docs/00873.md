# 读取旧数据磁带，艰难的方式

> 原文：<https://hackaday.com/2018/10/07/reading-old-data-tapes-the-hard-way/>

那些生活在软盘出现之前的计算机大容量存储时代的人很可能犯过这样的错误:将含有数据的盒式磁带放入立体声走带设备中。扬声器没有听到预期的令人敬畏的混音，而是发出令人讨厌的咩咩声，在两个不和谐的音调之间颤抖，无疑破坏了气氛。

你可能听说过的是堪萨斯城标准，这是为新兴的微型计算机行业提供大容量存储标准的早期尝试。它非常成功，直到今天你仍然可以找到需要解码的 KCS 录音带。这项工作对微控制器来说轻而易举，这也是为什么[matseng]选择艰难地完成这项工作，只用分立元件构建了[KCS 解码器。](https://github.com/SmallRoomLabs/KCSviewer)

目标是将频移键控(FSK)信号解码成 8 位并行输出，当字符以 300 波特的惊人速度从磁带上下来时，可能驱动 7 段显示器。原理图中看不到集成电路；正如[matseng]所说，除了“Qs、Rs 和 Cs”之外，什么也不是。所有需要的放大器、触发器和计数器都是由大量晶体管组成的，甚至七段显示屏也是由 3D 打印和热粘合框架中的 led DIY 而成。下面的视频显示了显示器尽力显示编码在录音带上的字母数字字符。对于那些绝对需要 Arduino 的人，[matseng]使用了一个 Arduino 和一个死虫低通滤波器来模拟 KCS 信号，以便于开发。

我们总是很欣赏那些选择更少人走的路来找到解决方案的黑客，但是如果你时间紧迫，无法解码一些 KCS 的磁带，那就不用担心了——[你所需要的只是一台电脑和勇气。](https://hackaday.com/2016/04/12/dump-your-old-computers-rom-using-audacity/)

 [https://www.youtube.com/embed/Zs1BC_5-5ak?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Zs1BC_5-5ak?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

