# Arduino IDE 2.0 在这里

> 原文：<https://hackaday.com/2022/09/28/arduino-ide-2-0-is-here/>

Arduino 发布了他们的集成开发环境(IDE)的最新版本，[2.0 版](https://blog.arduino.cc/2022/09/14/its-here-please-welcome-arduino-ide-2-0/)，这是上一个版本的一大进步，拥有许多新功能，可以帮助您更轻松地开发代码。

作为初学者进入编程硬件的实际方式，更有经验的用户有时会抱怨他们所看到的过于简单的 IDE——甚至缺乏相对基本的功能，如自动完成。新版本提供了这一点，除此之外还有更多。

Arduino 的新闻稿提供了一些主要功能的线索，但真正的细节隐藏在一系列新教程中，旨在让您快速了解新外观。

![Arduino IDE v2.0 remote sketchbook](img/66d1ea43f91d554fc58335f254c3d1a5.png)

主屏幕以不同的方式组织，以展示新的功能，并使开发更快更容易。新的“远程 Sketchbook”已经与 [Arduino Cloud](https://cloud.arduino.cc/) 紧密集成，以允许在开发期间在计算机之间轻松切换。V2.0 将自动拾取任何云草图，而使用以前版本 IDE 的计算机仍然可以像以前一样通过 [Web 编辑器](https://create.arduino.cc/editor)访问草图。

串行绘图仪现在可以与文本串行监视器同时使用，而不必选择其中之一。此外，对于那些支持它的设备，还有许多新的调试功能。这适用于常见的在线仿真器(如 [Atmel ICE](https://www.microchip.com/en-us/development-tool/ATATMEL-ICE) )，但也适用于较新的 Arduino 板，如 [Arduino Zero](https://store.arduino.cc/products/arduino-zero) ，无需任何额外的硬件。调试器让您可以访问强大的功能，如断点、单步执行和单步调试，以真正了解您的代码在做什么。

[![Arduino IDE v2.0 serial plotter](img/fd3d23c685892ddd0a6cd71c9481eb67.png)](https://hackaday.com/wp-content/uploads/2022/09/potentiometer-plotter.gif) 安装很简单，会自动拉入你在 Arduino 软件以前版本中创建的任何库和草图，以简化过渡。

新的 IDE 有很多值得喜欢的地方，但是我们预计需要一点时间来发现和有效地使用所有的新特性。其中一些是我们几年前讨论过的" [Arduino Pro IDE](https://hackaday.com/2019/10/21/the-arduino-ide-finally-grows-up/) "的延续，但是很高兴看到软件随着时间的推移而发展和改进。

你试过新的 IDE 了吗？你认为它与旧版本或其他开发环境相比如何？请在评论中告诉我们。

更新:感谢[亚历山德罗·拉内鲁西]在评论中指出新版本的主要优势之一是命令行工具 [arduino-cli](https://github.com/arduino/arduino-cli) 允许用户在他们最喜欢的编辑器中编辑代码，并在终端上调用“arduino-cli compile -u”来构建项目。

感谢[cardboardBaron]的提示。