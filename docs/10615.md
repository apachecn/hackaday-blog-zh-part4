# 用微控制器识别鸟声

> 原文：<https://hackaday.com/2021/07/06/recognising-bird-sounds-with-a-microcontroller/>

机器学习对于保护研究来说是一个不可思议的工具，特别是对于像长期观察和筛选大量数据这样的场景。虽然普通的黑客读者可能无法在某处孤立的荒野中参与数据收集，但我们都被鸟类生活所包围。使用 Arduino Nano 33 BLE 传感器和在线机器学习工具，一个由[埃罗尔·约书亚]、[阿吉特·库玛尔·KJ]、[马赫什·纳亚克]和[苏普里亚·尼克姆]组成的团队演示了如何设置一个自动鸟叫分类器。

Arduino Nano 33 BLE 感应是一款功能齐全的小型开发板，采用功能强大的 NRF52840 微控制器和蓝牙低能耗技术，以及各种板载传感器，包括麦克风。对许多人来说，训练一个机器学习模型似乎令人生畏，但像 [Edge Impulse](https://www.edgeimpulse.com/) 这样的在线服务使这个过程对初学者非常友好。一旦你开始为特定的应用训练自己的模型，你很快就会发现建立和维护高质量的数据集通常是机器学习中最耗时的部分。对于这个用例来说幸运的是，在 [Xeno-Canto](http://urlm.co.uk/www.xeno-canto.org) 上有一个来自世界各地的鸟叫的大规模在线图书馆。这可以用来自设备将被部署的区域的背景噪声来增强，以减少假阳性。Edge Impulse 将使用提供的数据集训练模型，并生成一个库，该库可以在 Arduino 上使用提供的样本草图之一来记录收集的数据并将其发送到服务器。接下来是不断迭代测试和改进识别模型的过程。如果你想要更密集的机器学习模型，Edge Impulse 也可以兼容更强大的设备，如 Raspberry Pi 和 Jetson Nano。

我们也看到完全相同的设置被用于智能婴儿监视器。如果你想了解更多，请务必观看[【肖恩·海默】在 2020 年远程会议](https://hackaday.com/2020/12/04/remoticon-video-how-to-use-machine-learning-with-microcontrollers/)上关于微控制器上的机器学习的演讲。

 [https://www.youtube.com/embed/LKvqgjf0byc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LKvqgjf0byc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



Joey Smith 在 Unsplash 上的标题照片

[hack adayprize 2021](https://prize.supplyframe.com)主办单位:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)