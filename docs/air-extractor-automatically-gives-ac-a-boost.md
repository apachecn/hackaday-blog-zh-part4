# 抽气器自动给空调增压

> 原文：<https://hackaday.com/2021/06/03/air-extractor-automatically-gives-ac-a-boost/>

在炎热的夏季，便携式空调是一种很好的降温方式，但它们需要一些地方来吹走从房间里带走的热量。[VincentMakes]为他的家准备了一台便携式空调，但是他发现他想把它放在离他唯一可以用来排放热空气的窗户太远的地方。在热空气排气管上有太长的管道会增加风扇上的背压，这可能会导致它过早出现故障，所以[【Vincent】使用了一个排风扇来自动增加空调装置的排气到窗户的速度。](https://hackaday.io/project/179232-air-extractor-controller-for-ac)

因为他的空调可以在低、中和高速下运行，所以他选择了一个也支持多种速度的排风扇，并注意匹配空调和排风扇的气流，以避免给任何一个风扇带来太大的压力。他设计了一个系统，使用霍尔效应电流传感器测量交流设备的功率消耗，并使用 Arduino Nano 进行控制，自动设置增压风扇的速度，以匹配交流设备的速度。一个定制的 PCB 将 Nano 与霍尔传感器和控制继电器连接起来，我们不得不称赞[Vincent]让+5V DC 和 230V 交流电彼此远离。除了这些精细的电子工作，【Vincent】还为风扇控制器建造了一个外壳，允许风扇以一定角度安装在顶部，这有助于避免排气管中出现硬弯曲。

如果这让你想到今年夏天用智能空调来保持凉爽，那就试试[这款由 ESP8266 供电的智能空调系统](https://hackaday.com/2019/06/11/smarten-up-your-air-conditioning-with-the-esp8266/)，或者[这款基于树莓派的系统，它可以控制空调和百叶窗！](https://hackaday.com/2013/12/07/raspi-ac-and-blinds-controller/)