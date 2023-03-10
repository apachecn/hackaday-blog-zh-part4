# 尖叫信道攻击射频安全

> 原文：<https://hackaday.com/2018/07/27/screaming-channels-attack-rf-security/>

自从有了无线电，人们就想偷听无线电广播。在许多情况下，这只是一个爱好活动，就像收听扫描仪或监控本地中继器一样。但在某些情况下，它是间谍机构或网络黑客。[Giovanni Camurati]和他的同事一直在研究一种略有不同的方法来攻击蓝牙无线电通信，这种方法使用的技术也可以应用于其他无线电类型。这种攻击依赖于混合信号 IC 的普遍使用，以制造像蓝牙加密狗这样的廉价无线电。他们称之为“[尖叫频道](http://s3.eurecom.fr/tools/screaming_channels/)”，简而言之，它依赖于设备无线电信号中泄露的数字信息。

有用吗？该小组声称在 10 米外找到了一把 AES-128 密钥。这项技术让我们想起了《暴风雨》( TEMPEST )( T1 ),因为无意的无线电传输提供了对设备加密或解密数据的算法的洞察。大多数(如果不是全部的话)加密技术都假设你看不到“黑盒”内部。如果可以，那是因为破解代码相对容易。

一些简单的实验(以及设备时钟频率的知识)让该团队能够可视化加密数据和非加密数据之间的差异。使用软件定义的无线电技术，他们攻击了 Nordic Semiconductor nRF52832 设备，在该设备中，他们能够轻松找到与单笔交易相对应的信号部分。当攻击者可以使用类似于[chip whisper](https://hackaday.com/2014/10/29/the-hackaday-prize-interview-with-a-chipwhisperer/)的东西来测量能量时，在恢复密钥方面已经做了一些工作，该团队能够利用这项工作。然而，与 ChipWhisperer 不同的是，尖叫通道不需要与设备进行物理连接。

奇怪的是，这并不像你想象的那么新。一位二战时期的贝尔研究员注意到，他可以通过观察示波器上的噪音来检测远程操作的密码机，并可以读取机器正在处理的文本。一旦他们证明这是一个真正的威胁，他们设计了一个笨重且难以部署的解决方案。军队忙于打一场战争，所以他们只是指示部队保持密码机周围的区域畅通，以防止这种攻击。不过，密码机最终会被屏蔽，以防止这种攻击。

问题是现在你在一个芯片上有了你需要花几便士制造的所有东西。防范这种攻击将需要相当多的重新设计，并且可能需要分离 RF 和数字数据电路。或者，市场可以像军队那样，决定接受风险。

随着越来越多不开发安全系统的人尝试这样做，我们可能会看到很多安全原则的重新发明。市场可能还会忽略低风险的问题。毕竟，许多手机都有指纹扫描仪，尽管[那些已经被黑客破解了](https://hackaday.com/2017/04/27/fundamentals-of-fingerprint-scanning/)超过 15 年。