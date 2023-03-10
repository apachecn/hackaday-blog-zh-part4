# 一个脱离网格的即时消息平台

> 原文：<https://hackaday.com/2020/07/02/an-off-the-grid-instant-messaging-plattform/>

拥有一个独立于任何网络、免费工作的开源通信设备，听起来像是黑客的梦想成真。嗯，这正是[bobricius]的 Armawatch 和 ARMA chat 设备的目标。

最近，[bobricius]开发了一款基于 LoRa 的即时通讯设备，名为 Armachat。这个小工具由一个带本机 USB 的 SAMD21 MCU 控制，包括一个 QWERTY 键盘和一个 LCD 显示器。通信基于 RFM95 LoRa 收发器，在理想条件下可达 2 公里范围。[bobricius]是 PCB 设计方面的奇才，他的项目看起来如此出色的一个原因是他经常使用 PCB 作为外壳。

Armachat 有两种外形，一种是大尺寸的台式电脑，另一种是小尺寸的袖珍版。新的 Armawatch 是另一个缩小版，通过使用更小的显示器和键盘，完美地适合你的手臂。[bobricius]也在固件上做了很多工作，现在具有消息传递确认和自动重新发送未传递消息的可能性。未来的改进将包括消息加密、存储转发功能和 GPS 位置解析。[bobricius]还在致力于完成他的信用卡大小的通信器产品组合。

LoRa 是[离网通信设备](https://hackaday.com/2019/03/24/custom-lora-pager-designed-with-care/)的首选技术，并且已经有其他正在进行的项目使用它来[构建网状网络](https://hackaday.com/2020/02/26/lora-mesh-network-with-off-the-shelf-hardware/)。

The [HackadayPrize2020](https://prize.supplyframe.com) is Sponsored by:[![Supplyframe](img/193ca31946d20fcfa39296cb816a4c50.png)](https://supplyframe.com/)[![Digi-Key](img/4fc24a8a6b4498aecfe987b00009d192.png)](https://www.digikey.com/)[![Microchip](img/8dd361210bbb0e5592c24f87e4e2267e.png)](https://www.microchip.com/)[![Arm](img/7d728b281b85469ef9013d45001f14b4.png)](https://www.arm.com/)