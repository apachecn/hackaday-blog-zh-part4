# 全波段无线电使用 Arduino 和 Si4730

> 原文：<https://hackaday.com/2020/02/12/all-band-radio-uses-arduino-and-si4730/>

越来越难区分自制项目和商业项目。一个很好的例子是[Mirko 的] [全波段无线电](https://create.arduino.cc/projecthub/mircemk/diy-si4730-all-band-radio-lw-mw-sw-fm-1894d9)，你可以在休息时间下面的视频中看到。从外面看，它有一个好看的外壳。在内部，它使用 Si4730 无线电，具有分立元件难以达到的出色性能。

该芯片包含两个带 AGC 的 RF 带，内置转换器，可在模拟和数字之间来回转换，并且片上还有一个 DSP。该芯片将进行 64 至 108 MHz 的调频，并可以解调 153 kHz 至 279 kHz、520 kHz 至 1.71 MHz 和 2.3 MHz 至 26.1 MHz 范围内的 AM 信号。它甚至可以读取无线电数据系统和 RBDS 电台信息。输出可以是数字(多种格式)或模拟。

无线电接受串行(I2C)命令，Arduino 转换用户界面，以便您可以控制它。这种芯片有几种口味，每种都有略微不同的特点。例如，Si4731 和 Si4735 具有 RDS/RBDS 解码器，Si4734 和 Si4735 提供短波模式。迷茫？编程指南第 2 页应该有所帮助。根据[Mirko]的说法，他使用的是 4730，但它仍然可以与 4735 库进行短波通信。

带芯片的分线板只要几块钱。看起来该芯片具有接收单边带的技术能力，但它需要一个记录不良的补丁。不过，这是最近版本的[本库](https://github.com/pu2clr/SI4735)。

当我们想到自己还活着的时候，我们总是会微笑。也许这是第一个[水晶无线电项目](https://hackaday.com/2018/01/19/a-modern-take-on-the-crystal-radio/)的现代版本。

 [https://www.youtube.com/embed/zPlVdLj5gFg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zPlVdLj5gFg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

