# UECG——一款非常小的可穿戴式 ECG

> 原文：<https://hackaday.com/2019/11/08/uecg-a-very-small-wearable-ecg/>

[终极机器人]一直致力于设计和生产一种极小的能够实时传输数据的心电图。

典型的心电图设备体积庞大:小型化对医院来说没有太大作用，因为医院的优化倾向于耐用性、寿命和易用性。通常一束导线串在导电垫和模拟前端和解释数据的显示器之间；非常清楚地将患者识别为测量对象。

uECG 将所有这些放在一个手指大小的包装中。毫不奇怪，这在罗马的[Maker Faire](https://hackaday.com/2019/10/25/giant-leds-ruby-lasers-hologram-displays-and-other-cool-stuff-seen-at-maker-faire-rome/)上引起了我们的注意，并且他们是[黑客日奖决赛入围者之一](https://hackaday.com/2019/09/10/meet-the-20-finalists-in-the-2019-hackaday-prize/)。电池、微控制器和采样电路几乎都封装在电路板上。用户可以选择以 125 Hz 的频率通过 BLE 传输数据，或者使用无线电收发器传输 1 kHz 的数据。即使以这些采样速率传输并过滤掉无用噪声信号，该器件的功耗也低于 10 mA。

制作设备的文件都在他们的页面上。尽管他们计划小批量生产电路板，这应该是获得电路板并开始试验这些有趣数据的最佳方式。

The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)