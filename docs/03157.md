# serialport 的功能与您想象的完全一样

> 原文：<https://hackaday.com/2019/05/30/serialplot-does-exactly-what-you-think-it-does/>

串行端口仍然是黑客的惯用手段，是将少量数据从一台机器转移到另一台机器的最简单方法之一。所有类型的项目都使用该接口，并且通常连接传感器，通过这种连接读取它们的数据。在这些情况下，绘制所述数据会很有用，[而 SerialPlot 就是一个可以做到这一点的工具。](https://bitbucket.org/hyOzd/serialplot/src/default/)

SerialPlot 能够一次通过几个串行端口读取数据，并绘制出来供您查看。它能够解释各种整数和浮点格式的数据，并以同步方式绘制多个通道。它还能够通过串行端口发送基本命令，用于触发或控制附加设备。

总的来说，对于通过最经典的接口连接一系列传感器的人来说，这是一个有用的工具。当然，如果你在跟踪你所有的串行端口时遇到困难，[有一个实用程序可以帮助你](https://hackaday.com/2019/05/22/windows-utility-helps-id-serial-ports/)。