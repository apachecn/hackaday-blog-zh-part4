# 辛克莱·ZX 的键盘接口

> 原文：<https://hackaday.com/2019/08/10/a-keyboard-interface-for-your-sinclair-zx/>

20 世纪 80 年代早期的辛克莱·ZX 8 位计算机是经济的杰作，最大限度地利用了最小的硬件。盒式磁带接口是一个一位端口，视频(至少在前两个型号上)是由处理器本身而不是 CRT 控制器创建的，键盘呢？这里没有花哨的键盘控制器，只有一个按键矩阵和一些位于一组地址线和一些数据线之间的二极管。ZX80 和 ZX81 的速度不是很快，因为它们的处理器与所有这些工作都有关系，但这确保了它们的零售价格可以在英国市场上突破 magic 100 大关，这在 1980 年是一个壮举。

[![](img/494be2146a73d9405b9916b2a73be0ae.png)](https://hackaday.com/wp-content/uploads/2019/08/arduino-nano-zx-spectrum-ps2-keyboard-mapping-1.png) 许多黑客仍然将他们的时间投入到这些机器上，其中【丹乔维奇】已经[更新了 ZX 键盘，在那个矩阵和 PS/2 键盘](https://hackaday.io/project/166917-tek-v2)之间产生了一个接口。正如你所料，它使用了现代的微控制器板，在这种情况下，Arduino Nano，但它没有发挥想象力，认为配备 USB 的板可能会执行相同的任务。它位于相关的线路上，并根据来自相连的 PS/2 键盘的串行输入，在它们之间执行必要的逻辑连接。该项目详细介绍了 PS/2 到 ZX 的映射，但最令人感兴趣的可能是它对所涉及的总线计时的解释。Arduino 利用 ZX 等待线来等待 Z80，并确保它有足够的时间来执行其任务，值得注意的是这是否对基本程序计时有明显的影响。

我们更习惯于看到 ZX 键盘连接到个人电脑上，而不是反过来。

ZX 光谱图像:比尔伯特伦[ [CC BY-SA 2.5](https://commons.wikimedia.org/wiki/File:ZXSpectrum48k.jpg) 。