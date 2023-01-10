# 简单的短波试验板 SDR

> 原文：<https://hackaday.com/2022/08/26/simple-breadboard-sdr-for-shortwave/>

了解无线电的最好方法之一是自己制作，即使在廉价 SDR 加密狗的时代也是如此。【Aniss Oulhaci】用一个简单的 [HF SDR 接收器演示了这一点，该接收器构建在试验板上](https://www.youtube.com/watch?v=G8BIYIsh-4I)。

接收器采用简化的泰勒检波器的形式。一个[射频前置放大器电路](https://www.onetransistor.eu/2015/12/hf-vhf-antenna-amplifier-without-coils.html?m=1)放大来自[短波天线](https://hackaday.com/2020/04/12/homebrew-loop-antenna-brings-the-shortwave-world-to-you/)的信号，并将其馈入一个 74HC4066D 模拟开关，该开关充当开关混频器。它将输入信号与本地振荡器的 [I 和 Q 信号](https://hackaday.com/2019/11/15/dsp-spreadsheet-iq-diagrams/)混合，以产生中频信号。本振由 SI5351 时钟发生器和 74HC74D 触发器组成，用于产生 I 和 Q 对。信号经过低通滤波器级，由 LM358 运算放大器放大，从而将 IQ 信号对馈入计算机的立体声声卡。

Arduino 用于控制 SI5351 时钟发生器，后者又由为 [SDR 屏蔽](https://hackaday.com/2020/02/14/rf-shield-turns-arduino-and-pc-into-shortwave-radio)创建的相同程序控制。随着音频信号进入 HDSDR，[Aniss]能够接收到短波无线电广播。

虽然这绝不是一个高性能的接收器，但在试验板上构建 SDR 仍然是一个很好的周末项目，有很多进一步实验的潜力。

 [https://www.youtube.com/embed/G8BIYIsh-4I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/G8BIYIsh-4I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

