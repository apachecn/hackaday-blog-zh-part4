# 把长笛的声音变成乐谱

> 原文：<https://hackaday.com/2019/12/29/turning-sounds-from-a-flute-into-sheet-music/>

作曲可能相当困难——毕竟，你必须记住音乐理论的所有要素，从拍号和调号到所有音符的正确长度。康奈尔大学微控制器设计班的一组学生开发了一个解决这个问题的方法，他们将长笛的声音转录成乐谱。

该项目不只是检测播放的音符，它能够将原始音频转换为标准化的乐谱，并配有准确的音符计时和每分钟节拍。在转录音乐之前，一些音频处理是必要的。由于其复杂的共轭极点，该团队选择使用 Sallen-Key 滤波器来放大原始音频输入。然后，他们使用快速傅立叶变换(FFT)来确定输入音符的频率，将信号从时域转换到频域。

该算法对数据进行采样以产生输入信号，利用微控制器上的 ADC 接收来自麦克风的输入。它获取采样信号的实部和虚部，并输出一对对应于采样频率的实部和虚部幅度分量，间隔均匀，从 0 到奈奎斯特速率(采样速率的一半)。这些箱的间距和具有最大振幅的箱用于将信号转换回真实频率和 MIDI 音符。

![](img/22da7149849025cd64053c858ff29547.png)

系统使用 PIC32 作为逻辑。麦克风放大电路使用一个增益为 50 的同相运算放大器，将麦克风输出信号幅度从 15 mV 提高到 750 mV，以供微控制器的 ADC 使用。然后，信号被发送至抗混叠 Sallen-Key 滤波器，其极点为 2.5 kHz，Q 为 1。选择该频率是因为 FFT 以 8 kHz 采样，并且该频率对应于笛子范围之外的音符。至于滤波器，只有低通滤波器用硬件实现。虽然带通滤波器可以在硬件中实现，但该团队决定采用更简洁的软件方法。

该项目在团队的[项目页面](https://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2019/lpr46_tev22_dms486/lpr46_tev22_dms486/lpr46_tev22_dms486/index.html)上有很好的记录，当然值得查看关于键盘控制和音频处理软件方面的更详细讨论。如果您想了解更多有关 FFT 的信息，请查看 2016 年[hack aday 奖的 FFT 频谱分析仪参赛作品](https://hackaday.com/2016/07/06/hackaday-prize-entry-open-source-fft-spectrum-analyzer/)。

 [https://www.youtube.com/embed/7qzfAA90V8g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7qzfAA90V8g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

