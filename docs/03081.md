# Eurorack Synth 模块在 ESP32 上运行

> 原文：<https://hackaday.com/2019/05/24/eurorack-synth-module-runs-on-esp32/>

ESP32 以其无线通信能力以及微控制器平台的强大处理能力而闻名。[[Robert Manzke]利用硬件开发了一个 Eurorack 音频合成平台，具有一些重要的功能。](https://hackaday.io/project/165365-eurorack-audio-synthesis-platform)

作为一个基准测试项目，[Robert]将 ESP32 与处理音频的 WM8731 编解码器芯片和 MCP3208 模数转换器相结合。这为平台提供了立体声音频，以及处理 8 个控制电压输入的能力。

由此产生的硬件组合成了[Robert]所说的 CTAG strmpler。这是一个基于采样的合成器，具有丰富的功能集，提供一些严肃的声音乐趣。除了所有常见的功能外，由于 ESP 的 WiFi 连接，它还具有通过互联网连接到 freesound.org 数据库的能力。这意味着新的样本可以通过它的 LCD 屏幕界面直接放入 synth。

由于 ESP32 中集成了大量的电源和外设，我们看到它用于一些真正令人印象深刻的音频项目只是时间问题。它还能做一些令人印象深刻的游戏。休息后的视频。

[hack adayprize 2019](https://prize.supplyframe.com)主办单位: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip) 

 [https://www.youtube.com/embed/zmj8tKPHV8g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zmj8tKPHV8g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

