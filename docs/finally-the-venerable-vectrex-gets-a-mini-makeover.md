# 最后，古老的威格斯得到了一个迷你改造

> 原文：<https://hackaday.com/2022/03/29/finally-the-venerable-vectrex-gets-a-mini-makeover/>

似乎每一个伟大的主机都注定会有一个微型翻拍:我们已经有了 PlayStation Classic，迷你 NES 和 SNES，甚至还有一个微型世嘉创世纪/Mega Drive。但是有一款很棒的游戏机在列表中缺失了，至少[Brendan]是这么认为的，那就是 Vectrex。因此，他着手[建造了一个全功能微型威格斯控制台](https://hackaday.io/project/184595)。

如果“Vectrex”这个名字在你的脑海中没有印象，你并不孤单:这是一个商业失败，在 1983 年视频游戏崩溃后，它很快被大多数人遗忘。但它在发烧友中仍然保持着狂热的地位，因为它的独特设计具有单色矢量显示器，你可以在其上放置透明覆盖物以获得某种彩色显示。它的游戏现在都可以使用 RetroPie 这样的软件来模拟，这就是[Brendan]选择在他放在周围的 Raspberry Pi Model 2 上运行的软件。

[![](img/461cab05e20e316d2051dea9b3fe2fc9.png)](https://hackaday.com/wp-content/uploads/2022/03/vectrexmini_detail.jpg) 至于显示屏，他看中了一款兼容 Pi 的 3.5 寸 TFT 设备。将它连接到 Pi 上很容易，但是让图像以正确的纵向方向呈现却非常令人头疼，需要不停地摆弄驱动程序和配置文件。

一旦他得到了这个工作，【Brendan】开始设计一个 Vectrex 的原始外壳的微缩模型。在他的 3D 打印机上进行了几次迭代和几次 10 小时的运行后，他最终得到了一个坚固的外壳，可以安全地将 Pi 及其显示器固定在适当的位置。几个小时的打印后，他也有了一个手持控制器，这是他基于 Arduino Pro Mega 设计的。Arduino 读取四个常规按钮和一个操纵杆，并通过一根盘绕的 USB 电缆与 Pi 通信。

最终的结果，正如你在下面的视频中看到的，是我们见过的最可爱的小 Vectrex。真的和[这个大屏 Vectrex 项目](https://hackaday.com/2017/11/02/finally-a-big-screen-vectrex/)正好相反。我们还看到[一台 Vectrex 投影仪](https://hackaday.com/2019/01/23/the-vectrex-projector-weve-been-waiting-for/)，甚至[一台真正的彩色显示器被黑进](https://hackaday.com/2018/01/03/vectrex-finally-in-color/)。

 [https://www.youtube.com/embed/NwqCw-uSZJ0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NwqCw-uSZJ0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

