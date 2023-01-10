# 你的手电筒是流明骗子吗？构建一个 DIY 积分球

> 原文：<https://hackaday.com/2022/02/07/is-your-flashlight-a-lumen-liar-build-a-diy-integrating-sphere/>

一盏灯曾经是很简单的事情:只要把一根灯丝插在一个玻璃灯泡里，让电流通过它，你瞧！让那里有光。更大的灯意味着更大的灯丝，需要更多的能量和更大的外壳。现在我们又向前看了一点，都是关于 led 的。真的没有“只是一个 LED”这样的东西，这些是半导体器件，由相对奇异的材料制成(好吧，反正不只是普通的旧硅)，有相当多的品种可供选择，选择它们有点复杂。

对于[Torque Test Channel]来说，从电能到辐射功率(或通量)的转换效率是感兴趣的主要数字，这促使他们[购买一堆灯来比较](https://www.youtube.com/watch?v=J0bYsF7h6lY)。公平地说，这需要一个业内称为[积分球](https://en.wikipedia.org/wiki/Integrating_sphere)(又名乌布里切特球)的东西，但作为一个专业设备，它对家庭游戏玩家来说有点昂贵。所以很自然地，他们决定自己建造这个东西。

[![](img/1b6a2ae553cf8160e7a3baa7a02fb336.png)](https://hackaday.com/wp-content/uploads/2022/02/diyintegrating_detail.jpg)

Coating the inside of the foam sphere took several attempts.

首先，他们做了明智的事情，将他们的测试单元运送到一个配有“合适”设备的计量实验室，以获得校准基准。接下来，他们开始使用一些相当普通的材料来建造他们的球体。基本的想法很简单；它有一个均匀的漫射内表面，确保光源发射的所有光子都可以在适当的测量端口进行测量，而不管它们从光源发射的角度如何。这样，总辐射功率可以被确定，或者至少被估计，因为会有一定程度的吸收。

总之，在几次错误的内表面涂层后，他们得出结论，将硫酸钡混合到涂料中，然后用砂纸打磨一下，就可以得到所需的纯白色漫射表面。

他们使用插入另一个端口的流明计进行测试，结果显示他们测得的流明值和实验室确定的流明值之间有很好的对应关系。由于 1 勒克斯被定义为每平方米 1 流明，他们似乎很幸运，发现他们的观察值和实验室值之间的比例是 10 比 1。这个因素将仅仅是由于他们的装置的物理设置，但无论如何，这是一个令人鼓舞的结果。那底线呢？这些测试设备是否达到了承诺的流明输出？看起来他们确实做到了。

下雨时，倾盆大雨。就在几个小时前，我们看到了另一种建造积分球的 DIY 方法，这次使用了一个所有东西的小炮弹模型。在此之前，我们实际上没有看到太多的光测量项目，[保存这个旧的使用芯片套件](https://hackaday.com/2014/04/24/measuring-light-with-chipkit/)。

 [https://www.youtube.com/embed/J0bYsF7h6lY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/J0bYsF7h6lY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢[赞]的提示！