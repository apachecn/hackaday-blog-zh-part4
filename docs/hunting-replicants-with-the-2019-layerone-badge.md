# 用 2019 LayerOne 徽章猎杀复制人

> 原文：<https://hackaday.com/2019/06/04/hunting-replicants-with-the-2019-layerone-badge/>

《银翼杀手》向我们展示了遥远未来洛杉矶的反乌托邦大都市景象。1982 年的 theater-goes (2019)是一个遥远的梦想，现在是我们的日常生活。我们知道洛杉矶不会永远阴云密布，飞行汽车不会在天空巡航，复制人也不会藏在人群中。或者……是他们吗？

LayerOne 会议在大洛杉矶举行，今年它采用了 T2 银翼杀手 T3 的主题来纪念这部里程碑式的电影。这个主题中我最喜欢的部分是模仿沃伊特-坎普夫机器的会议徽章。这些在电影中被用来区分复制人和人类，这也正是这个徽章的作用。在电影中，通过问问题和监测他们的眼睛反应来测试复制人——这个徽章有一个可选的眼睛识别相机来提供这种效果。我们来看看吧！

## 沃伊-坎普夫徽章

![](img/30e9a66f1946338c714c729fddddcc37.png)

完整的 Voight-Kampff 机器是一个手提箱大小的控制台，不适合挂在挂绳上，所以每个与会者收到的都是一个闪闪发光的 LED 电路板。除了*layer on 2019*标志，它的形状和前表面来自电影机器外围设备，用一个邪恶的发光中心盯着嫌疑人。这里的中心是一个由六个橙色 LED 组成的阵列，在一个透明的塑料圆顶下以催眠模式循环，伴随着一个缓慢闪烁的蓝色 LED 和一个快速闪烁的红色 LED。

[![](img/58111e19d187d03b0d2b8af0e9e7eb42.png)](https://hackaday.com/wp-content/uploads/2019/06/LayerOne-2019-badge-logo-LED-strip.jpg) 但是那个*layer on 2019*的标志是我们发现真正表达 2019 年 LED 背光 PCB 艺术的地方，通过电路板基板发出灯光表演。将徽章翻过来，我们看到标志的背面被可单独寻址的[侧发光二极管](https://hackaday.com/2019/04/17/the-science-of-reverse-mounted-leds/)所包围，这是 PCB 艺术家在这次展示中最受欢迎的。(标有“B+”和“B-”的焊盘为可选的附加模块供电，我们稍后将介绍该模块。)

[![](img/3c0d3beb9286ccdf68b2e6917c4b3b65.png)](https://hackaday.com/wp-content/uploads/2019/06/LayerOne-2019-badge-reverse.jpg)

从那个详细的视图中缩小，我们发现一个 ATtiny2313 从它的中央指挥所指挥所有的灯光。喂养它的 LED 军队是一个 18650 锂离子电池的工作，我们在角落里用一个微小的滑动开关召唤灯光秀。我最初以为电源开关附近的 IC 是一个稳压器，但它实际上是一个 APM4953 双 MOSFET，可以比一个微型开关更好地处理 18650 的电流。显然，船上的一切都是在电池电压水平下运行的。

这是一件有趣的会议饰品，如果有人想要更多，组织者已经准备了可选的附加套件。在 LayerOne，每项活动都旨在为初学者提供友好的介绍，并增加难度，以挑战资深人士。通过这种方式，我们觉得尝试新事物是受欢迎的，无论我们喜欢多少。在电子硬件的情况下，初学者通过插入电池和扳动开关打开徽章来加入 blinky 的乐趣。我对这第一步不满意，所以我加热了烙铁，并开始使用相机附加套件。

## 眼睛识别照相机模块

 [![LayerOne 2019 M5Cam parts](img/78746089cb16350bf2f352ba89b48e30.png "LayerOne 2019 M5Cam parts")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/05/LayerOne-2019-M5Cam-parts.jpg?ssl=1)  [![LayerOne 2019 M5Cam installation](img/a5e85c206e252290f0f9caea4f3f326e.png "LayerOne 2019 M5Cam installation")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/05/LayerOne-2019-M5Cam-installation.jpg?ssl=1)  [![LayerOne 2019 M5Cam installed](img/8a89e5c89c6a562f35d7697f95fd9ebd.png "LayerOne 2019 M5Cam installed")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/05/LayerOne-2019-M5Cam-installed.jpg?ssl=1) 

摄像头附加套件是围绕 M5Stack 的 [ESP32CAM 模块构建的。它通过两根焊接线从会议徽章上获取能量。一个 3D 打印的支架将模块固定在适当的位置，借助两个螺钉和一个小扳手将所有东西固定在一起。一旦组装好，我就可以启动一个配套的 iOS 应用程序，它接收相机的视频，并在视图中寻找一只眼睛。如果发现一只眼睛，则提取该眼睛的正方形视频，并将其覆盖在电影的静止帧上。现在徽章的作用更像是一台沃伊特-坎普夫机器。](https://m5stack.com/products/m5stack-official-esp32-camera-module-development-board-ov2640-camera-type-c-grove-port-3d-wifi-antenna-mini-camera-board)

[![](img/76ebe3c634efca4dbcaf5328d74a0a68.png)](https://hackaday.com/wp-content/uploads/2019/05/LayerOne-2019-Badge-iOS-companion-app-800x450.jpg)

## 徽标套件是 SMD 焊接挑战

随着令人毛骨悚然的眼睛扫描仪完成，我转移到 LayerOne 标志针。

 [![LayerOne Logo LED kit badge parts](img/9a4d177f7ed9f69220884538c624f70e.png "LayerOne Logo LED kit badge parts")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/05/LayerOne-Logo-LED-kit-badge-parts.jpg?ssl=1)  [![LayerOne Logo LED kit badge MCU](img/dbdb650bc36b16d21bd7aa06de9b97b6.png "LayerOne Logo LED kit badge MCU")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/05/LayerOne-Logo-LED-kit-badge-MCU.jpg?ssl=1)  [![LayerOne Logo LED kit badge LEDs](img/cbbd2d1617933b8379affe86bfe53df9.png "LayerOne Logo LED kit badge LEDs")](https://i0.wp.com/hackaday.com/wp-content/uploads/2019/05/LayerOne-Logo-LED-kit-badge-LEDs.jpg?ssl=1) 

[![](img/0bb3e24886d142a8985bb4348e170fad.png)](https://hackaday.com/wp-content/uploads/2019/05/LayerOne-2019-LED-blinky.gif) 这是一个小巧的发光二极管引脚，装在一个装有所有表面贴装器件和一块裸板的拉链袋中。去年在[的 LayerOne](https://hackaday.com/2018/05/29/badge-bling-and-more-at-layerone-2018/) 我接触了 SMD 焊接，这被证明是一次很好的技能回顾和测试。

最困难的部件是用于机器放置的 ATtiny2313 in 无情 MLF (QFN)封装。包括我自己在内的许多人都努力想把它焊接好，但是通过耐心和稳定的手，它最终被安装到位。通过这个挑战后，套件中的其他一切都相对容易，成功的形式是一个简单的 LED 二进制计数器。

任何希望更深入探索这些项目的人都可以参考发布在他们的 [Github 库](https://github.com/charlie-x/layerOne2019)上的参考信息。最起码，为徽标套件创建不同的图案会很有趣，而且 ESP32 相机模块有很大的未来项目潜力。或许有人会利用这些受沃伊特-坎普夫启发的作品，建造一个[全套复制设备](https://hackaday.com/2017/02/12/blade-runners-voight-kampff-test-gets-real/)！