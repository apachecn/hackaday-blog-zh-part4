# 简单，独立的劳拉中继器大约一个小时

> 原文：<https://hackaday.com/2019/05/02/simple-self-contained-lora-repeater-in-about-an-hour/>

![](img/52b8e09e616b378438abbabe86b43860.png)[Dave Akerman]对高空项目的兴趣意味着他对长距离无线通信并不陌生，LoRa 在这方面非常有用。LoRa 是一种以相对较低的数据速率和较低的功率进行长距离传输的方法。

尽管 LoRa 的范围很大，但有时设备的传输(如气球着陆的有效载荷)无法直接接收，因为它太远了，或者隐藏在建筑物和地理位置的后面。在这些情况下，一个有用的解决方案是[Dave]的[独立 LoRa 中继器](http://www.daveakerman.com/?p=2469)。中继器的硬件很简单，[戴夫]说，如果手头有零件，它可以在大约一个小时内建成。

该设备只需重新传输它收到的任何遥测数据包，所需要的只是一个 Arduino Mini Pro 和一个小型 LoRa 模块。一个小小的 DC-DC 转换器、电池和电池充电器完善了材料清单，创建了一个小型的独立单元，可以在桅杆上升起，放在风筝上飞行，或由无人机携带。

中继器的频率和其他设置甚至可以重新编程(使用一个小的 windows 程序)以获得最大的灵活性，这使得这个小设备在寻找着陆的有效载荷时变得非常宝贵，就像[戴夫]使用[使用塑料模型和高空气球](https://hackaday.com/2018/02/11/plastic-model-emulates-the-first-untethered-spacewalk/)重新创建一个著名的 NASA 图像一样。查看项目的 [GitHub 资源库的详细信息，并开始在您最喜欢的经销商处将零件“添加到购物车”中。](https://github.com/daveake/LoRaRepeater)