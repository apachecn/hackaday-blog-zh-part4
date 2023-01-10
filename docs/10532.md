# 制造调幅发射机和接收机的许多方法中的一些

> 原文：<https://hackaday.com/2021/06/25/some-of-the-many-ways-to-build-am-transmitters-and-receivers/>

AM 收音机是相对简单的设备，制造一台是开始探索无线电通信世界的好方法。[GreatScott]在休息之后的视频中完全做到了这一点[，建立了一个发射器和接收器。](https://www.youtube.com/watch?v=khXwzBW2sHI)

在最基本的层面上，AM 收音机的工作原理是用振荡器产生载波，然后用音频信号调制振幅。围绕这些部分，每当事情开始振荡时，古老的 555 定时器总是被提起；因此，你无疑会很高兴地看到[GreatScott]决定尝试他的第一次实验，测试两个流行的 555 发射机电路。一个使用控制电压引脚输入音频信号，另一个使用 reset 引脚。CV-pin 版本稍微好一点，但仍然几乎不可能区分标准商业 AM/FM 接收器上的声音。

下一次尝试是使用 XR2206 函数发生器套件，当与简单的麦克风放大器电路结合使用时，效果相当好。但这一次，接收端被替换了，因为[GreatScott]围绕 TA7642 AM 放大器/解调器 ic 构建了一个基本电路，只有六个无源元件和一个手绕线圈。

构建 AM 收音机的方法并不缺乏，这些年来我们已经讨论了不少。当然，一个 [555 定时器也可以用在一个接收器](https://hackaday.com/2011/02/25/hear-that-its-a-555-timer-am-radio/)中，只使用分立元件构建发射器相当简单，正如 [10 分钟发射器](https://hackaday.com/2021/03/11/getting-on-the-air-with-a-10-minute-ish-ham-transmitter/)和[单晶体管发射器](https://hackaday.com/2021/01/20/a-one-transistor-ham-transmitter-anyone-can-build/)所展示的那样。

 [https://www.youtube.com/embed/khXwzBW2sHI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/khXwzBW2sHI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

