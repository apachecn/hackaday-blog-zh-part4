# 通过视觉识别天线

> 原文：<https://hackaday.com/2022/11/01/identify-that-antenna-by-sight/>

这是一项业余无线电爱好者多年来学会的技能，但有时会令人惊讶地发现，并非每个人都有这种技能，即随意扫一眼天线杆或屋顶上的天线，就能猜出它的用途。当然，我的意思并不是凭直觉就能从稀薄的空气中解码出无线电信号，而是我们大多数人看到一根天线，就能立即收集到许多有关其频率和性能的信息。这种特权知识是在授予业余无线电爱好者执照的秘密仪式上从埃尔默家族传下来的吗？一点也不，事实上，留下来，我会分享一些窍门。

## 重要的是尺寸。

[![Anthorn radio station](img/344c47aca020b71b65ac928b459604d1.png)](https://hackaday.com/wp-content/uploads/2022/10/anthorn-radio-station.jpg)

A very low frequency needs a very large antenna. [Anthorn radio station](https://en.wikipedia.org/wiki/Anthorn_Radio_Station), here viewed from about three miles away, has one of the largest antennas in the UK for its 19.2kHz submarine transmitter. Even then it’s not a full quarter-wavelength.

我们通常认为频率是兆赫，有时是千赫或千兆赫。但是频率硬币的另一面是以米为单位的波长，它在自由空间中传播一周的长度。以光速传播的无线电波的一个功能是，频率对应于光在一秒钟内传播的距离所能适应的周期数。因此，如果我们把光的速度看作是 3 10^8 米每秒，那么，这意味着波长是 3 x 10^8 除以频率赫兹。该公式的一个更实用的版本是，300 除以以兆赫为单位的频率得出以米为单位的波长，因此，例如，100 兆赫的波长是 3 米。频率越低，波长越长，因此低频天线比高频天线大。

知道了特定频率的波长，我们就能立即掌握使用该频率所需的天线尺寸，但这并不像为 100 MHz 设计一个 3 米长的天线那么简单。相反，原型天线使用波长的一部分，通常是一半或四分之一，因此立即识别天线类型的元素开始发挥作用。你需要磨练猜测不同尺寸的技巧，因为通常有一个桅杆或其他容易测量的结构作为参考是很有用的。

## 我在看什么

[![A dipole antenna](img/b019cda52a5a76f59fa9f7ab96723723.png)](https://hackaday.com/wp-content/uploads/2022/10/dipole-antenna.jpg)

The description says that this dipole is for “1 to 4 GHz”, but looking at this we’d guess it’s set up for 1 GHz, roughly 15cm long. Schwarzbeck Mess-Elektronik, [CC BY-SA 3.0](https://commons.wikimedia.org/wiki/File:Half_%E2%80%93_Wave_Dipole.jpg).

许多读者对最基本的天线设计都很熟悉，如偶极天线，两个导体各有四分之一波长长，排成一条直线，中间连接一根同轴馈线。这种天线衍生出许多其他设计，因此知道如何在这些其他天线设计中发现它，可以让您立即了解该频率的四分之一或半波长有多长。因此，100 兆赫的天线是 3 米波长的一半，即大约 1.5 米长。如果你环顾四周的屋顶，直到你看到有人用调频收音机偶极天线为 88 至 108 兆赫，然后，它会在某处大约这个大小。

[![An FM boradcast Yagi antenna](img/43e164fab3cf9020f573a3de0a4abe86.png)](https://hackaday.com/wp-content/uploads/2022/10/fm-radio-yagi.jpg)

An FM broadcast Yagi antenna. Sanjo, [Public domain](https://commons.wikimedia.org/wiki/File:JOZZ0BA-FM_Antenna_closeup.JPG).

如果你环顾屋顶、公用建筑和其他地方的天线，你会发现很少有偶极子天线。它们中的许多都是长而尖的事物，一个中间的吊杆，一串与之成直角的元素，或者一个三角形的元素阵列，沿着一个中间的吊杆。屋顶电视天线是这种类型的一个很好的例子，以其发明者的名字命名为八木宇田阵列。他们开始创建一个使用无线电波的无线能量传输系统，结果发现他们自己创建了一个高度定向的阵列，其中一个偶极子由一组无源元件连接。偶极还是一样的，所以如果你能估计它的大小，你就能找到频率。

[![A log-periodic antenna](img/91952c0ef21e955af2818342aca2eef3.png)](https://hackaday.com/wp-content/uploads/2022/10/1280px-Schwarzbeck_UHALP_9108_A.jpg)

A log-periodic antenna. This one is good for 250 to 2400 MHz. Schwarzbeck Mess-Elektronik, [CC BY-SA 3.0](https://commons.wikimedia.org/wiki/File:Schwarzbeck_UHALP_9108_A.jpg).

还有另一种类似于八木宇田阵列的天线，除了特有的三角形外，看起来极其相似。这是一种被称为对数周期的宽带天线，它是不同频率的偶极子阵列。然而，如果你能估计每个偶极子的大小，就有可能通过观察最大和最小的偶极子来计算出频率的分布。

八木天线和对数周期天线都是定向的，所以除了计算出它的频率，你还可以知道它正在通信的站在哪里。有一次，我骑着摩托车在牛津郡的小巷里寻找当地乡村水厂的基站，度过了一个略感愉快的夏日午后。通过这种方式，每个水厂都在一个小桅杆上安装了一个 450 MHz 的八木天线。通过在地图上排列它们，我能够找到控制点，毫不奇怪，它位于我所在的小镇的污水处理厂。

还有最后一种天线，你会在车辆和其他地方看到很多，垂直或鞭状天线。其中最简单的是一根四分之一波长的弹性线，很容易猜测频率，但有几个复杂因素会使猜测偏离方向。你经常会看到鞭状天线的线圈在底部或中间的某个点，这些可以是负载或相位线圈，以改变天线的性能。通常，它们有助于将较大的天线装入较小的空间，这使得总长度不太有用。如果有一个秘密，那就是大多数业余爱好者已经看到了足够多的天线，通过与我们看到的天线进行比较，我们可以识别出困难的天线。抱歉，也许你真的需要一棵榆树来把它传下去。

头球:来自荷兰鲁尔蒙德的伯特·考夫曼 [CC BY 2.0](https://commons.wikimedia.org/wiki/File:Barcelona_(2624027495).jpg) 。