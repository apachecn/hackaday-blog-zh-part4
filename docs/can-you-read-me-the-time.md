# 你能给我读一下时间吗？

> 原文：<https://hackaday.com/2019/09/21/can-you-read-me-the-time/>

如果你喜欢普通的时钟用户，你可能已经厌倦了阅读模拟时钟。通常，解决方案只是使用一个数字时钟，但[【sjm 4306】](https://www.youtube.com/user/sjm4306)选择制作一个[小单词时钟](https://hackaday.io/project/164406-small-word-clock)，无论你去哪里，它都可以用英语提醒你时间。

与[【戈丹·威廉姆斯】](https://hackaday.com/2019/02/15/is-that-a-word-clock-in-your-pocket/)的类似项目不同，该项目使用 8 x 8 的 LED 矩阵和喷墨打印覆盖层，这款小型文字时钟使用 3D 打印的灯箱来实现其字母矩阵。事实上，他们的灵感来自所有现有的 DIY 单词时钟设计，使用现成的 LED 阵列，透明遮罩和 WS2812s。

该设计采用自制 PCB 设计，通过 USB 提供 5 V 电源。该设计将字母放在顶部挡板上，并限制层，以防止阻焊膜和铜阻挡光线。底部使用相同的设计原理，方形与字母重叠。为了阻挡相邻字母之间的光线，3D 打印的灯箱开始发挥作用。

![](img/deced6c201b15c76575df334bfb1261e.png)

字母矩阵的一个设计挑战是将所有可能的分钟放入数组中。[sjm4306]没有制作更大的字母阵列，而是让时钟以五分钟为间隔来描述时间，然后添加星号来表示完整的时间。这是一个非常容易理解的保持设计简单的解决方案，所有的字母都非常适合这个设计！

![](img/d171e85fb3359c66622f6ca9578548bf.png)

使用分配给阵列的行和列的 I/O 的管脚映射，软件将管脚的状态切换为 switch 语句。为了扫描矩阵，软件使用中断来绘制当前的 led 列，并在增加到下一列之前更新显示图像。通过跳过或不跳过周期，这允许显示器看起来更亮或更暗。

时间跟踪相当简单，使用 DS1302 串行实时时钟芯片——它甚至为超级电容器充电，以在断电后保持时间！

为了处理 PCB 的 FR4 材料内部散射的光，使用分离器来容纳光。作为一种低成本的解决方案，虽然仍然有一些光扩散，但肯定比没有分离器要好。

几乎所有用于构建小型字时钟的文件都可以在[sjm4306]的项目页面上找到，包括软件和设计文件。希望用不了多久，我们就会看到更多这种低成本的字钟设计！

 [https://www.youtube.com/embed/fYtS_n_GhCY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fYtS_n_GhCY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2019](https://prize.supplyframe.com) is Sponsored by: [![Supplyframe](img/79a7db035b8a2b6c2b7b0895c45b7de8.png)](https://supplyframe.com/)  [![Digi-Key](img/ba094a14c430ab81591a2abdc54a5363.png)](https://hackaday.io/digikey)  [![Microchip](img/5023ef0b7ff1aee311cba9b54a3ac9fe.png)](https://hackaday.io/microchip)