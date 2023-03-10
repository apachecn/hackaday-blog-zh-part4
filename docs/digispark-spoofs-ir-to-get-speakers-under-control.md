# Digispark 欺骗 IR 来控制扬声器

> 原文：<https://hackaday.com/2020/11/24/digispark-spoofs-ir-to-get-speakers-under-control/>

Microlab 6C 是一对相当不错的扬声器，但[michas omkowski]对它们待机时消耗的 8 瓦并不太满意。简单的解决办法是在不用的时候拔掉插头，但不幸的是，前面板上的数字控制意味着他必须打开它们，选择正确的输入，并在每次插回插头时将音量调到合适的水平。肯定有更好的方法。

他的解决方案是[使用 Digispark 发射适当的红外遥控代码](https://slomkowski.eu/projects/microlab-speakers-remote-hijack/),这样它们就会自动回到可用的配置。但他没有在 GPIO 引脚上安装红外 LED，而是简单地将其连接到扬声器红外接收器的引线上。他的代码需要做的就是在线路上产生适当的脉冲，扬声器的电子设备认为这是来自遥控器的信号。

[![](img/d65b14bd419ca0672a90e74effc75c27.png)](https://hackaday.com/wp-content/uploads/2020/11/microlab_detail.jpg)

Distinctive patterns on the IR sensor wires.

Digispark 的电源来自扬声器本身，所以一旦[micha]插上电源，它就会打开。代码等待五秒钟，以确保硬件有时间启动，然后继续执行“通电”、“更改输入”和“提高音量”命令，每一个命令之间都有几秒钟的间隔。

不仅跳过 IR 直接注入信号更容易，而且安装也更干净。由于微控制器不需要红外接收器的视线，[micha]能够将其隐藏在扬声器的外壳内。从外面看，改装是完全看不见的。

我们已经看到了在之前使用的[类似的代码注入技巧，这绝对是你应该记住以备将来参考的技巧之一。尽管越来越多的](https://hackaday.com/2020/03/06/esp8266-adds-web-control-to-old-home-theater/)[现代设备正在接受 WiFi 和蓝牙控制](https://hackaday.com/2020/10/28/replace-your-ir-remote-with-a-web-browser/)，老式的红外遥控器似乎不会很快消失。