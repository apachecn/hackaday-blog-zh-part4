# 智能温度计先探测，后提问

> 原文：<https://hackaday.com/2019/09/18/smart-thermometer-probes-first-asks-questions-later/>

随着流感季节侵入北半球，医生办公室和免预约诊所将被痰多的人挤满，他们问自己一个古老的问题:是流感，还是只是有点感冒？要是他们家里都有智能温度计，能分辨出不同就好了。

一般来说，成人低于 101 华氏度(38.5 摄氏度)，儿童低于 100.4 华氏度(38 摄氏度)的发烧被认为是轻度的，因此可能不是流感。但是在苦难的时候，谁能记得这些事情呢？[M. Bindhammer]的[如果 EVE 是一个救生的医疗设备，消除猜测](https://hackaday.io/project/164757-ifeve)。它通过安装在背部的 3D 打印耳朵探针读取数据，然后问一系列是/否的问题，如您是否有畏寒、疲劳、咳嗽、喉咙痛等。然后 Teensy 3.2 使用朴素贝叶斯分类给出流感与感冒的概率。[M.]选择的红外温度计精度为 0.02°C，所以应该是一个相当可靠的指标。

最终的决定当然应该由医生办公室的咽拭子来决定。但是这种智能温度计的广泛使用可能是减少流感死亡的第一步，并且可能会提高医生与病人的比率。

[hack adayprize 2019](https://prize.supplyframe.com)主办单位: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)