# 无线锡罐电话

> 原文：<https://hackaday.com/2020/06/08/wireless-tin-can-telephone/>

对于许多孩子来说，锡罐电话是一个有趣的科学实验，它不会持续很长时间，就像把线缠在附近的树上一样。[杰夫]决定另辟蹊径，制造一部完全无线的铁罐电话。

构建从黑客最喜欢的 Arduino Uno 开始。它连接到一个麦克风输入板，该输入板使用 Arduino 的模拟输入来拾取音频。Arduino 然后通过 NRF24L01+无线收发器将这些数据发送出去，由另一端相应的锡罐接收器接收。LM386 被赋予放大器的功能，连接到一个小扬声器上，这样用户就可以听到传入的音频。

Arduino Uno 绝不是一个高保真数字音频平台，但该项目确实提供了一些清晰的，如果粗糙的语音传输。它也是学习无线电通信和处理数字音频信号的好方法。NRF24L01+是为项目添加无线通信的绝佳方式，如果您正在寻找更大的覆盖范围，[我们也能满足您的需求](https://hackaday.com/2015/08/15/hacking-a-nrf24l01-radio-for-longer-range/)。休息后的视频。

[hack adayprize 2020](https://prize.supplyframe.com)主办单位:[![Supplyframe](img/193ca31946d20fcfa39296cb816a4c50.png)](https://supplyframe.com/)[![Digi-Key](img/4fc24a8a6b4498aecfe987b00009d192.png)](https://www.digikey.com/)[![Microchip](img/8dd361210bbb0e5592c24f87e4e2267e.png)](https://www.microchip.com/)

 [https://www.youtube.com/embed/E-2zu7KqG40?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/E-2zu7KqG40?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[hack adayprize 2020](https://prize.supplyframe.com)主办单位:[![Supplyframe](img/193ca31946d20fcfa39296cb816a4c50.png)](https://supplyframe.com/)[![Digi-Key](img/4fc24a8a6b4498aecfe987b00009d192.png)](https://www.digikey.com/)[![Microchip](img/8dd361210bbb0e5592c24f87e4e2267e.png)](https://www.microchip.com/)