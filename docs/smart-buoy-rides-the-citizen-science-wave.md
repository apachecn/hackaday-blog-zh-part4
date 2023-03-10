# 智能浮标驾驭公民科学浪潮

> 原文：<https://hackaday.com/2019/09/11/smart-buoy-rides-the-citizen-science-wave/>

那些美丽而危险的海浪把我们召唤到海岸边，不仅仅是一道美丽的风景。它们能告诉我们许多关于天气模式和海洋本身正在做什么的信息。尽管这些信息非常重要，但是现有的波浪研究方法非常昂贵。[t3chflicks]的团队希望证明这可以相当便宜地实现，以鼓励更多的公民科学家做出贡献。更多的数据意味着更好的理解，开放的研究甚至让那些不积极参与的人受益。

他们开发了一种智能浮标，可以收集海浪数据，并将其传输回基站进行实时显示。浮标运行在 18650 上，由位于 3D 打印船体上半部分周围的四块 5V 太阳能电池板充电。浮标内部的 Arduino 控制传感器，其中大部分传感器都被安装在 GY-86 10 自由度模块中。顶部的天线将数据发送回 Raspi Zero 基站，该基站在漂亮的 Vue JS 仪表板上实时绘制波高、波周期、波功率、水和空气温度以及气压。

在这个项目中，团队经历了起起落落。他们想测量波浪方向，但事实证明这有点太复杂了。内存问题使他们无法将数据备份到浮标上的 SD 卡中。你可以在他们的 YouTube 频道上看到更深入的硬件和软件视频。休息后，我们将智能浮标摘要视频捆绑在一起，开始播放。

想帮助 buoy wave 研究，但是没有 3D 打印机？密封的聚氯乙烯是一个很好的漂浮设备，正如我们在[中看到的这个水质感应浮标](https://hackaday.com/2017/11/29/intellibuoy-keeps-track-of-the-water/)。

 [https://www.youtube.com/embed/S-XMT6GDWk8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/S-XMT6GDWk8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[hack adayprize 2019](https://prize.supplyframe.com)主办单位: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)