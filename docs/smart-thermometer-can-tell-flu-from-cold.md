# 智能体温计可以区分流感和感冒

> 原文：<https://hackaday.com/2020/06/26/smart-thermometer-can-tell-flu-from-cold/>

在冠状病毒爆发之前，季节性流感是最危险的传染病之一，但许多人很难仅凭症状区分流感和感冒。这给了[M. Bindhammer]设计一个智能体温计的想法，它可以区分流感和感冒。

自动化医疗诊断无疑是未来的一项[重要技术。[M. Bindhammer]的项目名为 F LUEX，是他的](https://youtu.be/hmUVo0xVAqE) [iF EVE 温度计](https://hackaday.io/project/164757-ifeve)的第二个版本。测完体温后，它会问病人一系列关于他的症状的问题，然后计算出更有可能是流感还是感冒的概率。[M. Bindhammer]使用一种基于贝叶斯统计的医学诊断中常用的方法，该方法为两种假设分配一个概率分数。它考虑了当你患普通感冒或流感时，某种症状出现的频率，以及感染这两种疾病的总体概率。

该项目的硬件基于一个定制的 PCB，其中包括一个医用级 MLX90614 红外温度计，其精度约为人体体温的 0.2˚。传感器由一个 3.2 英寸的传感器读出，信息显示在一个小的有机发光二极管屏幕上。一切都装在一个 3D 打印的外壳中，通过涂上底漆和丙烯酸喷漆进行了漂亮的整理。不幸的是，[M. Bindhammer]项目也因电晕危机而推迟，因为他的温度传感器订单因当前的高需求而被取消。但这确实让我们想知道这对于区分感冒、流感和新冠肺炎有多大用处。

红外温度计不仅在医疗应用中非常有用，而且[也可以在没有定制 PCB 和最小部件的情况下制造](https://hackaday.com/2019/04/30/a-stylish-low-part-count-non-contact-thermometer/)。

The [HackadayPrize2020](https://prize.supplyframe.com) is Sponsored by:[![Supplyframe](img/193ca31946d20fcfa39296cb816a4c50.png)](https://supplyframe.com/)[![Digi-Key](img/4fc24a8a6b4498aecfe987b00009d192.png)](https://www.digikey.com/)[![Microchip](img/8dd361210bbb0e5592c24f87e4e2267e.png)](https://www.microchip.com/)[![Arm](img/7d728b281b85469ef9013d45001f14b4.png)](https://www.arm.com/)