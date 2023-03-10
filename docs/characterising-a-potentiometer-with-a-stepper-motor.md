# 用步进电机表征电位计

> 原文：<https://hackaday.com/2019/04/21/characterising-a-potentiometer-with-a-stepper-motor/>

电位计或可变电阻是我们习以为常的标准元件。如果容量罐上写着“10k log ”,那我们就装了，然后就忘了。但如果你像(本·霍姆斯)一样在模拟电子音乐电路，就需要更多的知识。为此，他创建了一个用于表征电位计的装置，以生成电位计值的查找表。

这是一个足够简单的设置，其中一个电压控制的电流源为电位计供电，而一个带电机控制器的 Arduino 通过步进电机转动电位计，并通过模拟引脚从其游标读取电压读数。也许大多数读者可以在相当短的时间内组装它。有趣的是它揭示了电位计的结构。

音频电位计通常是对数型的。也就是说，电阻的变化率在轨道的长度上是对数的，以便在例如音量控制中模仿人耳的对数音量响应。如果有人教你对数盆，你很可能会看到一条平滑的对数曲线，但正如他在下面的视频中发现的那样，事实并非如此。相反，它们表现为一组近似于对数曲线的线性部分，这可能更容易制造。知道这一点对[Ben]的模拟工作当然很有用，但对我们其他人来说，这是对电位计制造的一个迷人的洞察，并表明我们永远不应该把一切都视为理所当然。

 [https://www.youtube.com/embed/hoh-xfAEe_4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hoh-xfAEe_4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

