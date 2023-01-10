# PHONK——黑客对 Android 编程的有趣捷径

> 原文：<https://hackaday.com/2020/07/02/phonk-a-hackers-fun-shortcut-to-android-programming/>

众所周知，普通人只利用了智能手机真正潜力的 10%。尤其是当涉及到电子项目时，我们似乎经常忽略如何在这里集成和利用它们的功能。也许这并不令人惊讶——虽然这不是火箭科学，但进入移动开发肯定有其障碍，并需要一点承诺。[维克托·迪亚斯]认为一定有更好的方法，所以他继续创造了 [PHONK，这是为 Android](http://phonk.app/) 开发的*自含式创意脚本工具箱*。

PHONK 像其他应用一样安装，通过抽象和简化大量的样板文件、原生 Java 部分，允许通过 [JavaScript](https://en.wikipedia.org/wiki/Rhino_(JavaScript_engine)) 在你的 Android 设备上快速制作原型。因此，PHONK 不会从头开始建立一个应用程序，并定义所有的资源、UI 设计、活动和应用程序生命周期管理，更不用说 Android 开发环境本身了，而是在幕后处理所有这些事情，并显著减少完成您真正感兴趣的任务所需的代码量。如果你现在担心你必须在你的手机上实际编程，那么，你*可以*，这肯定可以派上用场，但你不必。

一旦应用程序打开，就会启动一个 web 服务器，从同一个 WiFi 网络中的任何现代浏览器连接到它，就会为您提供 PHONK 开发环境，其中包含您需要的一切:编辑器、文件浏览器、控制台和 API 文档。您可以在浏览器中编写代码，然后按下 run 按钮将直接在设备上执行代码。由于一切都是应用程序本身自带的，因此不需要额外的软件，您可以通过探索提供的示例集立即开始，这些示例展示了迄今为止支持的一切:传感器交互、BLE 服务器和客户端、MQTT 或 WebSockets 等通信协议、OpenStreetMap 地图，甚至与[纯数据](https://en.wikipedia.org/wiki/Pure_Data)和[处理](https://en.wikipedia.org/wiki/Processing_(programming_language))的集成。连接一根 USB OTG 线，你就可以对你的 Arduino 进行编程，进行串行通信，或者连接一个 [IOIO 板](https://en.wikipedia.org/wiki/IOIO)。你甚至可以连接一个 MIDI 控制器。

这是[Victor]完成的令人印象深刻的工作，在开发过程中对细节投入了大量精力。如果你有一部旧的 Android 手机正在某个地方积灰，这将是一个让它复活并利用它做点什么的好机会。正如[Victor]在该项目的 GitHub 页面上所写的，他总是好奇人们会提出什么。如果你正在考虑建立一个移动传感器实验室，或者想了解更多关于手机内部传感器的信息，[看看 36C3 关于 phyphox 的演讲](https://hackaday.com/2019/12/29/36c3-phyphox-using-smartphone-sensors-for-physics-experiments/)。