# 一个简单的流式无线电接收机

> 原文：<https://hackaday.com/2022/08/14/a-simple-streaming-radio-receiver/>

对于那些对广播电台职业感兴趣的人来说，进入这个行业的途径并不多。学生电台、海盗电台和医院电台通常出现在任何 DJ 简历的开头。医院的广播电台通常没有传输许可证，历史上一直依赖有线系统，但由于这些系统无法覆盖所有地方，他们现在更有可能依靠互联网。[AllanGallop]为英国城市 Milton Keynes 的[医院电台](http://mkhrs.org.uk/main/)创造了[迷你网络收音机](https://www.instructables.com/Mini-Web-Radio-ESP32/)，这是一个紧凑的电池供电的单站流媒体收音机，可以通过无线网络连接在任何地方接收这些音乐。

在设计整洁的 3D 打印盒内，硬件非常简单，一个 WeMos ESP32 板和一个 MAX98357A I2S 数字放大器模块，全部由 18650 电池供电。有一个音量控制和耳机插座，这是用户界面所需的一切。该软件具有 Arduino 和 Platform.io 的代码，并通过 web 界面进行配置，正如您所期望的那样。如果你想自己构建一个，你可以在一个方便的 GitHub 仓库中找到所有的东西。与此同时，作为一名黑客抄写员，展示一个植根于自己黑客空间的项目尤其令人愉快，在这种情况下，[Milton Keynes makers space](https://mkmakerspace.co.uk/)。

感谢[Cid]的提示！