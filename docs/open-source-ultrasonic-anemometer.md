# 开源超声波风速计

> 原文：<https://hackaday.com/2021/07/06/open-source-ultrasonic-anemometer/>

气象站是试验各种环境传感器的热门项目，对于风速和风向，通常选择简单的杯型风速计和风向标。为了【马建佳】的 [青站](https://hackaday.io/project/180079-qingstation-ultrasonic-anemometerweather-station) ，他决定打造另一种类型的风传感器:超声波风速计。

超声波风速计没有移动部件，但其代价是电子复杂性大大增加。他们的工作原理是测量超声波音频脉冲在已知距离内反射到接收器所需的时间。风向可以通过从两个相互垂直的超声波传感器对读取速度数据并使用一点简单的三角学来计算。为了使超声波风速计正常工作，需要在接收端精心设计模拟放大器，并进行大量信号处理，以便从二次回波、多路径和环境引起的所有噪声中提取正确的信号。设计和实验过程是 [请战](https://github.com/majianjia/QingStation/blob/main/doc/anemometer.md) 。由于[Jianjia]无法进入风洞进行测试和校准，他临时将风速计安装在车顶上，然后开车出去兜风。这产生的读数与汽车的 GPS 速度成比例，但稍高一些。这可能是由于计算错误，或外部因素，如风，或测试车或其他交通干扰气流。

其他传感器包括光学雨水传感器、光传感器、照明传感器和用于气压、湿度和温度的 BME280。[Jianjia]计划在自主船上使用 QingStation，因此他还包括了 IMU、指南针、GPS 和用于环境声音的麦克风。事实上，所有传感器都没有移动部件，这是该用例的一个主要优势，我们期待看到 boat 项目。所有的软硬件都是开源的 [在 GitHub](https://github.com/majianjia/QingStation) 上都有。

几年前，我们报道过另一种超声波风速计，但它有不同的传感器配置。如果你喜欢简单，更常见的杯型风速计可以用一系列废料制成，包括[旧硬盘部件](https://hackaday.com/2016/02/07/another-use-for-old-hard-drive-parts-anemometer/)和[塑料复活节彩蛋](https://hackaday.com/2019/01/08/an-electronic-love-letter-to-the-wind/)。