# 老式遥控器获得蓝牙升级

> 原文：<https://hackaday.com/2021/07/04/vintage-remote-control-gets-bluetooth-upgrade/>

这个时髦的 Magnavox 遥控器在红外线使用之前就已经足够古老了，实际上它依靠超声波与电视进行交流。这是一个很好的话题开始，但在今天不是很有用。这就是为什么[【Chad Lawson】决定去除原来的电子设备，代之以 Adafruit Feather 32u 4 blue fruit LE](https://www.instructables.com/Retro-Future-Bluetooth-Remote/)实际上可以与现代设备对话。

我们知道，我们知道。观众中的一些人可能会对这样一个很酷的小工具被毫不客气地拆开感到生气，但公平地说，[乍得]确实说他有第二个会保持原状。另外，在易贝上快速查看一下就会发现，这些旧遥控器似乎并不特别稀有或值钱。事实上，在浏览了最近结束的拍卖后，我们相当肯定他为这两个遥控器支付了 27 美元。

[![](img/f9e7797f94c2eb131e08db0e1ef27896.png)](https://hackaday.com/wp-content/uploads/2021/06/btremote_detail.jpg) 总之，【查德】发现他收藏的一块 perfboard 恰好和遥控器上的 PCB 差不多大，这让剩下的转换变得相当简单。他只需在 perfboard 的一侧安装触觉开关，这样当按下遥控器的原始按钮时就会触动它们，然后将它们连接到另一侧的 Adafruit。我们知道还有一块 3.7 V 500 mAh 的袋状电池，虽然现在还不清楚他把它藏在图像中的什么地方。

[Chad]想出的代码告诉 Adafruit 模仿蓝牙人机界面设备(HID ),并向与之配对的任何设备发送标准键码。例如，这使得它很容易在电脑上用作媒体遥控器。[如果你已经在零件箱里有了一个，并且想改造一个你自己的遥控器，我们已经在 ESP32](https://hackaday.com/2021/05/27/this-esp32-bluetooth-page-turner-cant-get-any-easier/) 上看到过类似的事情。

在文章的最后，[Chad]提到他可能会尝试开发一种超声波接收器，可以接收来自未经修改的遥控器的信号。这将是一个很好的方式，使整个事情完整的循环，并应安抚即使是最铁杆的老式遥控爱好者。