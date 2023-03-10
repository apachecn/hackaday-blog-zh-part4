# 2022 年 Hackaday 奖:Boondock Echo 将您的收音机与云连接起来

> 原文：<https://hackaday.com/2022/08/27/2022-hackaday-prize-boondock-echo-connects-your-radios-with-the-cloud/>

马克·J·休斯(Mark J Hughes )志愿加入当地社区消防队，通过无线电进行协调。洛杉矶的 La Habra Heights 地区是一个多峰多谷的地区，这使得直接无线电连接具有挑战性。中继器能很好地提高覆盖范围，但是在这样的地区，没有合适的地方来放置它们。[Mark]说，在紧急情况下(如野火),无线电使用量会激增，他会定期跟踪多达 8 个无线电频率，并尝试理解这些频率，同时研究如何向谁发送信息。

这让他和合作者一起创建了[项目 Boondock Echo](https://hackaday.io/project/186791-project-boondock-echo) ，以帮助减轻压力。这个概念是使用一个便宜的宝丰无线电馈入一个基于 ESP32 音频开发套件的网关。将它安装在一个装有 LiPo 电源的盒子里，你就有了一个可移动的无线电-云时移录音机。

[从那里，任何有访问权限的人都可以检索它们，无论其物理位置如何，只需要一个互联网连接。](https://hackaday.com/wp-content/uploads/2022/08/boondock_detail.jpg)

可以执行的下一个技巧是反转该过程，将以前的记录排队，并通过云将其发送回远程位置，以便通过无线电重新传输到现场。这显然是一笔巨大的资产，因为哪里有城市化，哪里就可能有互联网连接。由于增加了一个 Boondock Echo 单元，任何人只要在几英里之内有一个接收器，就可以完全与直接无线电通信范围之外发生的事情联系起来。

ESP32 固件的来源以及 web 方面的东西可以在[项目 Boondock Echo GitHub](https://github.com/kaushleshchandel/boondock) 中找到，其中包括一些用于 3D 打印盒子的 STL。像往常一样，解决特定问题的方法不止一种。这是一个基于 RTL-SDR 和 Raspberry Pi 的[业余无线电中继器。](https://hackaday.com/2016/12/05/an-amateur-radio-repeater-using-an-rtl-sdr-and-a-raspberry-pi/)

The [HackadayPrize2022](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)