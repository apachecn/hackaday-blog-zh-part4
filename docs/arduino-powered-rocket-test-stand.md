# Arduino 动力火箭试验台

> 原文：<https://hackaday.com/2018/12/14/arduino-powered-rocket-test-stand/>

如果你对业余火箭技术感兴趣，你很快就会超越玩具店出售的极小的埃斯特斯发动机。许多业余爱好者转而建造自己的自制固体火箭发动机，并对推进剂混合物进行实验，但很难知道你是否在正确的轨道上，除非你有办法量化你得到的推力。[【elemental maker】决定他最终需要为他的马达](https://www.youtube.com/watch?v=-yq1EmTkBCs)组装一个低成本的测试台，幸运的是，我们决定记录这个过程和结果。

[这种配置能够以 80Hz 的采样率测量高达 10 公斤的重量，这是至关重要的，因为这些类型的火箭发动机一开始只燃烧几秒钟。该传感器在燃烧的短暂时间内产生数百个数据点，非常适合绘制发动机的推力曲线。](https://hackaday.com/wp-content/uploads/2018/12/ardustand_detail.png)

鉴于测量的窗口如此之小，[元素制造者]不想留下任何侥幸心理。因此，支架上的 Arduino 会自动完成这两项工作，而不是手动点燃电机和触发数据收集。按下支架上的红色按钮，启动倒计时程序，LED 闪烁，之后继电器用于给插在电机内的镍铬合金线“电子火柴”通电。

在休息后的视频中，你可以看到[ElementalMaker]最初在让 Arduino 点燃点火器时遇到了一些问题，最终追踪到这个问题是由于电流过多，导致镍铬合金线熔断过快。将他最初使用的大铅酸电池换成一个简单的 9V 电池解决了这个问题，后来他在展台上的第一次测试燃烧获得了完全的成功。

如果模型火箭是你喜欢的东西，我们这里有足够的内容让你忙起来。在过去，我们已经[报道了建造你自己的固体火箭发动机](https://hackaday.com/2010/09/28/homemade-solid-propellant-rocket-motors/)以及[电子点火器来点燃它们](https://hackaday.com/2010/11/16/making-model-rocket-motor-igniters/)，甚至还有一个[无线测试台，让你在 T-0](https://hackaday.com/2015/10/12/wireless-rocket-motor-analyzer-tests-rockets-saves-fingers/) 时离行动更远一点。

 [https://www.youtube.com/embed/-yq1EmTkBCs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-yq1EmTkBCs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢 Baldpower 的提示。]