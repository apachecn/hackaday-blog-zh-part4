# PsyLink:一种用于无创肌电的开源神经接口

> 原文：<https://hackaday.com/2022/01/07/psylink-an-open-source-neural-interface-for-non-invasive-emg/>

我们没有看到很多 EMG(肌电图)项目，尽管这些应用程序可能很酷。这可能是因为在噪音中看到微小的肌肉电信号的技术困难，也可能是解释你找到的任何信号的困难。不管怎样，[hut]一直在努力推出一系列原型，[最终推出了名副其实的“原型 8”](https://psylink.me/)

目前的原型使用了一个主电源板来承载一个 [Arduino Nano 33 BLE 感应](https://store.arduino.cc/products/arduino-nano-33-ble-sense?selectedStore=eu)，以及一个升压转换器来给 AAA 电池充电，为 Arduino 和一系列连接的 EMG 放大器单元提供 5 伏电压。 [EMG 传感器](https://psylink.me/b3/)基于 [INA128 仪表放大器](https://www.ti.com/document-viewer/INA128/datasheet/device-images-dv#dv)，配置非常简单。EMG 样本以及来自 Nano 33 BLE Sense 上 IMU 的数据通过蓝牙传递到连接的 PC，运行 PsyLink 软件堆栈。这是基于 Python 的，使用[BLE-关贸总协定](https://pypi.org/project/BLE-GATT/)库进行 BT 通信， [PynPut](https://pypi.org/project/pynput/) 处理 PC 输入设备(发出键盘和鼠标事件)和 [tensorflow](https://www.tensorflow.org/) 进行机器学习。这个想法是使用来自 EMG 数据的机器学习来与特定的用户界面事件(例如按键)相关联，并且经过一点训练，能够在 PC 上仅通过手/臂手势玩游戏。IMU 数据用于增强这一点，但在这个演示中，这并不完全清楚。

[![](img/0abed0ce6263441280fafd560252303d.png)](https://hackaday.com/wp-content/uploads/2022/01/psylink_detail.jpg)

An earlier prototype of the PsyLink.

所有的硬件和软件都可以在 [project codeberg](https://codeberg.org/psylink/psylink) 页面上找到，这让我们不禁要问为什么要使用 [GnuRadio](https://www.gnuradio.org/) ，但是仔细想想，它对信号处理和可视化真的很好。多好的主意啊！

显然这种 EMG 控制的输入设备还有很多其他的用例，但是谁不想玩马里奥赛车呢，你知道，*科普*？

查看演示视频(嵌入在下面)，你可以自己看，只是要注意这是从 [peertube](https://joinpeertube.org/) 流出的，所以视频可能会有点断断续续，这取决于你当地的同行。最后，如果[乳齿象](https://joinmastodon.org/)是你的茶，[这里是那个](https://fosstodon.org/@psylink)的链接。早期的项目已经尝试过 EMG，比如来自颠倒实验室的生物放大器板。此外，我们还翻出了我们自己的[Bil Herd]关于主题的早期教程。]

[https://peertube.linuxrocks.online/videos/embed/f042e209-f3fd-4b92-8295-f91e8c46e861#?secret=vgR05jnzgR](https://peertube.linuxrocks.online/videos/embed/f042e209-f3fd-4b92-8295-f91e8c46e861#?secret=vgR05jnzgR)