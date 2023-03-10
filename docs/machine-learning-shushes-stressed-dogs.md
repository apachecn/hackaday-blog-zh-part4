# 机器学习嘘压力大的狗

> 原文：<https://hackaday.com/2021/11/15/machine-learning-shushes-stressed-dogs/>

如果有一个人在 Covid 锁定期间从被困在家里的人们中受益，那将是狗。他们的人类一周 7 天 24 小时都在意味着更多的肚子摩擦、更多的餐桌残羹剩饭和更多的关注。当然，对许多狗来说，尤其是那些在隔离期间找到家的狗，这导致了依恋问题，因为它们的人类同伴已经开始返回工作和学校。

[Clairette]有一段时间特别难以适应她的朋友每天离开，但谢天谢地她的人类[Nathaniel Felleke]能够想出一个聪明的解决方案。他训练了一个 TinyML 神经网络来检测她何时吠叫，并使用 Arduino 播放一个声音字节来安抚她。问题中的声音字节是[Nathaniel]的妈妈表扬或责骂[Clairette]的录音，正如你从下面的视频中看到的，它们似乎工作得很好。为了训练网络，[Nathaniel]使用了几个数据集来避免过度拟合，其中包括一个他自己使用自己房子里的狗叫声和环境声音的实际记录创建的数据集。他使用 Edge Impulse 的工具 Eon Tuner 来帮助找到使用和执行培训的最佳模型。他将训练好的网络上传到运行 Mbed OS 的 Arduino Nano 33 BLE Sense，第二个 Arduino 通过 Adafruit 音乐制作人 Featherwing 处理播放声音字节。

虽然机器学习听起来可能有点像抑制你的狗叫的极端解决方案，但它确实是创新的，甚至似乎已经成功了。搭配这个[联网的零食分配器](https://hackaday.com/2013/02/05/web-connected-treat-dispenser-appeases-the-pets/)，你可以让狗狗开心几个小时。

 [https://www.youtube.com/embed/v5hBjouFHQY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/v5hBjouFHQY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

