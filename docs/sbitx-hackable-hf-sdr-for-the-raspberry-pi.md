# SBITX:树莓 Pi 的可破解 HF SDR

> 原文：<https://hackaday.com/2021/08/06/sbitx-hackable-hf-sdr-for-the-raspberry-pi/>

便宜，易于使用的 SDR 加密狗是一个非常强大的学习无线电技术的工具。然而，建立自己的 SDR 并不是太多黑客有信心解决的事情。[Ashhar Farhan，VU2ESE]希望通过围绕 Raspberry Pi 设计的可破解 HF SDR 收发器 [sBITX](https://www.youtube.com/watch?v=9mFxyS6_2t8) 来改变这一点。

[Ashhar]在 QRP 业余无线电俱乐部国际的虚拟“五月的四天”年会上介绍了这个项目。休息后观看视频中的完整对话。他首先介绍了可用的开源 SDR 无线电，然后深入研究了他对 sBITX 的设计决策。该项目的主要目标之一是降低准入门槛。为此，他选择了 Raspberry Pi 作为基础，并编写了 C 代码，任何做过一点 Arduino 编程的人都应该能够理解和修改这些代码。硬件设计得尽可能简单。在接收端，使用简单的超外差架构将 25 kHz 宽的 RF 频谱片馈入音频编解码器，后者将数字化音频发送至 Raspberry Pi。然后使用 FFT 在软件中对信号进行解调。发射时，信号由软件产生，然后上变频至所需的 RF 频率。[Ashhar]还为 7 英寸的 Raspberry Pi 屏幕创建了一个 GUI。

目前，sBITX 仍处于开发阶段，信息在休息后的视频、伴随的 [PDF](https://drive.google.com/file/d/1PfAAVfHeX0WTaUqste2cKQcXkrs_HMWk/view) 、 [GitHub repo](https://github.com/afarhan/sbitx) 和 BITX20 组上的[线程之间传播。](https://groups.io/g/BITX20/topic/sbitx/83191173?p=,,,20,0,0,0::recentpostdate%2Fsticky,,,20,2,20,83191173)

[阿沙尔·法尔汉]在业余无线电爱好者群体中以低成本无线电设计而闻名，如 [BITX](https://hackaday.com/2016/10/18/the-bitx-transceiver-comes-of-age/) 及其继任者 [μBITX](https://hackaday.com/2017/03/14/ashhar-farhans-done-it-again/) 。他还创造了基于 Arduino 的天线测试仪 [Antuino](https://hackaday.com/2019/09/18/hackable-ham-radio-multitool-contributes-to-long-term-survival-of-the-hobby/) 。

 [https://www.youtube.com/embed/9mFxyS6_2t8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9mFxyS6_2t8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

