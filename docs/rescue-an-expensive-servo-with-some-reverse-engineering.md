# 用逆向工程拯救昂贵的伺服系统

> 原文：<https://hackaday.com/2019/12/11/rescue-an-expensive-servo-with-some-reverse-engineering/>

[Andrew]有人将电源连接到错误的引脚(哎呦)损坏了一个伺服系统，这烧坏了微控制器和逻辑电平转换器。通过一点逆向工程，[他通过编写一些新代码成功地恢复了基本的伺服功能](https://bytechlab.com/2019/07/reverse-engineering-herkulex-drs-0602-servo/)。新代码只实现了基本的功能，但这足以将设备从垃圾箱中拯救出来。

[![](img/790452a6d113dcd2301ee3441d876f54.png)](https://hackaday.com/wp-content/uploads/2019/12/Reverse-engineering-herkulex-drs-0602-motor-description-1024x683.jpg)

FAULHABER 2232DBHHO ring any bells? Google came up empty.

为什么要对伺服系统进行逆向工程呢？好吧，如果金钱是理由，那么有很多理由从垃圾堆中拯救一个 HerkuleX DRS-0602；他们在运输之前花费大约 320 美元。尝试的另一个原因是，微控制器原来是一个 AVR XMega，这给了[Andrew]编写一些新代码的信心。

如果你想更多地了解这些伺服系统是如何工作的，[安德鲁]提供了内部的良好照片，并确定了主要部件及其连接和功能。有一些谜团(如电机和嵌入式编码器的细节，这是 FAULHABER 2232DBHHO)但[Andrew]想出了足够的办法来编写一些基本代码，以允许伺服系统作为具有 UART 接口的标准伺服系统工作。

有时好奇心驱动逆向工程和修复工作，有时是成本，有时两者都有。一台 320 美元的伺服系统当然值得尝试去拯救，而配备过时伺服放大器的大型天文台望远镜也是如此。