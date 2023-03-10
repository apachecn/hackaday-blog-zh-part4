# Arduino 人的内部阴谋是一个谜

> 原文：<https://hackaday.com/2022/09/19/the-inner-machinations-of-the-arduino-are-an-enigma/>

Arduinos 是近二十年来微控制器平台的首选，本质上抽象了小型微控制器的大量设置和低级功能，以支持明智的 ide 和易用性。这为那些可能不愿意花数小时或数天时间埋头于数据手册的人提供了价格合理的微控制器，但也掩盖了一些有用的底层功能。但是如果你想深入了解它们，正如[Jim]在关于中断的系列文章的最后一篇中向我们展示的[，它们仍然在每件事情的下面工作。](https://escmdxi.wordpress.com/2022/08/16/speed-reading-ltc/)

在本操作指南中，[Jim]以不同的速度解码线性时间码(LTC)。该数据通常以音频形式传输，因此微控制器的响应需要快速。为确保数据正确解码，首先要对输入信号进行边沿检测。由于这是专门使用中断，Arduino 上的一个引脚专门用于在这些边沿触发中断。项目的其余部分包括设置中断服务程序，检测时钟信号，然后进行所有必要的处理，以便在小屏幕上显示接收到的 LTC。

项目页面详细介绍了这一切，包括正确设置所需的所有数学运算。就中断的一般用途而言，这是使用这些微控制器的底层功能的极好入门。如果你想看这个项目之前的其他两个项目，可以在[上找到它们，第一个特性是关于精度和准确度的](https://hackaday.com/2022/01/31/time-and-accuracy-in-las-atmegas/)，第二个特性是关于比特碰撞协议本身的[。](https://hackaday.com/2022/06/19/animate-arcane-protocols-with-interrupt-backed-bitbanging/)