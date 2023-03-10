# 袖珍 Deauther 肯定会给你带来麻烦

> 原文：<https://hackaday.com/2019/04/04/pocket-sized-deauther-could-definitely-get-you-in-trouble/>

干扰无线电通信，无论是通过干扰、解除授权攻击还是其他干扰，通常都被认为是一种犯罪，会受到严厉的处罚。然而，研究这样的技术应该在未来的电子战中提供一个有用的优势。在这种情况下， [[Giorgio Filardi]最近开发了一个信用卡大小的 WiFi deauther。](https://www.instructables.com/id/Credit-Card-Sized-Deauther-With-Oled-Screen/)

该设备有一个简单的界面，由 3 个按钮和一个小有机发光二极管屏幕组成。还可以通过 web 界面远程访问和控制它。NodeMCU ESP8266 板使用[spacehuhn]的 deauther 固件运行该节目。点对点结构可能经不起野外的颠簸，但对于台架测试来说还是不错的。如果要经常使用，我们建议建造一个围栏。

内置了大量功能——该设备可以扫描网络，执行拒绝攻击，甚至创建欺骗网络。这是一个棘手的小设备，它凸显了 WiFi 安全方面的几个缺陷，这些缺陷有待当权者修复。

出于邪恶目的使用这些设备可能会给你带来麻烦。然而，在你自己的网络上做实验是有教育意义的，这表明无线网络永远不会像我们希望的那样安全。

如果你想知道解除认证和干扰之间的区别，[这是你的入门书](https://hackaday.com/2011/10/04/wifi-jamming-via-deauthentication-packets/)。