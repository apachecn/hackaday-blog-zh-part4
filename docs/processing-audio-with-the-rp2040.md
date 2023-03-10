# 使用 RP2040 处理音频

> 原文：<https://hackaday.com/2022/04/17/processing-audio-with-the-rp2040/>

虽然 Raspberry Pi 最初是作为一种用于教育的廉价单板计算机，但现在它在电子社区中无处不在。其低廉的价格以及 Linux 平台和可访问的 GPIO 使其在课堂之外的许多地方都很有用。但是，如果你想放弃易用性而追求更低的价格，Raspberry Pi foundation 也可以通过 Pico 上常见的 RP2040 芯片实现这一点。[Jason]向我们展示了一种利用这种强大芯片的方法，即[将一个芯片放入音频数字信号处理板](https://hackaday.io/project/184811-ds-pi-rp2040-audio-dsp-board)。

虽然这种芯片有开发板，但[Jason]选择了他自己设计的定制 PCB，包括一个集成耳机放大器和 3.5 毫米音频插孔。为了完成实际的 DSP 工作，RP2040 芯片使用 3 个 12 位 ADC 通道和 16 个可控 PWM 通道。该平台还配备了德州仪器(ti)的 TLV320AIC3254 编解码器。综上所述，他有了一个功能正常的开源平台，他称之为 DS-Pi。

[Jason]将它作为一个吉他效果平台和一个可定制的吉他放大器建模器，但通过一个兼容 Arduino 且相当容易编程的平台，它可以用于任何涉及其他类型音乐或音频处理的事情，如[这个专门的 MIDI 兼容吉他效果平台](https://hackaday.com/2021/03/15/guitar-effects-with-no-unwanted-delay/)，它是围绕同一处理器构建的。