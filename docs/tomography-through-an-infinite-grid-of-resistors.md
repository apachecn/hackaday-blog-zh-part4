# 通过无限电阻网格的层析成像

> 原文：<https://hackaday.com/2019/04/06/tomography-through-an-infinite-grid-of-resistors/>

医学中尚未开发的巨大潜力之一是获得成像设备。10 亿人很难获得 x 光，这还不包括核磁共振成像和计算机断层扫描。在过去的几年里，[Jean Rintoul]一直在研究一种低成本的方法，只用几个电极就可以对人体内部进行成像。这种方法既便宜又简单，是将医学影像带给大众的最具创新性的方法之一。[现在，这是一个众筹项目](https://www.crowdsupply.com/mindseye-biomedical/spectra)，旨在为每个人提供安全、可访问的医学成像。

[![](img/a62c0151af5a24f4d0824de0159333d4.png)](https://hackaday.com/wp-content/uploads/2019/04/spectrabiomed.png) 它被称为 Spectra，使用电阻抗断层成像技术对胸腔内部、骨头的介电谱或草莓内部进行成像。Spectra 通过在身体的一部分缠绕一个电极并发出小的交流电流来做到这一点。这些小电流通过断层摄影技术重建，成像身体的横截面。

[Jean]在去年的 hack aday super conference 上做了一个关于 Spectra[的演讲，如果你想了解平价医疗技术的前沿，你不必再往前看了。简单地通过发送一个大约 10kHz 的交流波通过一个身体，软件可以重建内部结构。从肺体积到肌肉和脂肪量到癌症的一切都可以用这种设备检测出来。你仍然需要一名技术人员或医学博士来解释数据，但这是一种将医学成像技术带给需要它的人的好方法。](https://hackaday.com/2019/01/07/towards-low-cost-biomedical-imaging/)

现在，光谱是由大众提供的，有一个可以配置成使用 32 个电极的板。测量速度为 160，000 样本/秒，这些样本具有 16 位分辨率。虽然这只是采集硬件，但用于断层重建的软件是开源的，也很容易获得。

就将医学成像带给大众而言，这是一项令人印象深刻的工作，可能是去年 Hackaday 奖中最有可能改变世界的项目。