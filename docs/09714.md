# 实用传感器:霍尔效应

> 原文：<https://hackaday.com/2021/05/20/practical-sensors-the-hall-effect/>

测量磁场可能很容易，只需要一些很低的技术，也可能是很高的技术。这只是取决于你需要什么样的测量和你想付出多少努力。最简单的磁传感器是[簧片开关](https://hackaday.com/2018/03/01/mechanisms-the-reed-switch/)。这些基本上都是没有线圈的继电器。代替线圈的是一个外部磁铁，它足够靠近簧片来接通或断开触点。你可以在很多地方看到这种情况，比如门报警传感器。

话说回来，簧片没有真正的技巧。当它看到足够多的磁场时就会改变状态，仅此而已。你可以使用一个带有某种探测针的指南针来获得更多关于磁场的信息，但仅此而已。然而，这就是早期磁力计的工作原理。今天，你有很多选择，包括几乎无处不在的霍尔效应传感器。

你可以利用霍尔效应来测量键盘按键上的磁性按钮，当你按下它时，或者阀门的开关状态。许多霍尔效应被用作电流监视器。由于线圈产生的磁场与通过它的电流成正比，所以磁传感器可以在没有任何物理接触的情况下估计线圈中的电流。霍尔效应还可以观察磁铁在线性运动系统或旋转系统中经过，以获得位置或速度的概念。例如，看看这个无刷电机控制器，它使用[三个传感器来了解电机的位置](https://hackaday.com/2018/04/19/completely-scratch-built-electronic-speed-controller/)。

## 历史

[![](img/12192f67c84b1c9d58f30949ada5604f.png)](https://hackaday.com/wp-content/uploads/2021/03/hall.jpg) 埃德温·霍尔于 1879 年确定了这一效应。基本思想很简单:载流导体会因附近的外部磁场而发生变化。这些变化表现为你在导体上测量的电压。通常情况下，导体两端的电压几乎为零，但有磁场时，你会得到一个非零读数，这个读数与特定平面上的磁场强度成比例，我们很快就会看到。

霍尔效应传感器只是现代磁力计的一种。有许多不同的类型，包括那些使用感应拾波线圈，可以旋转或不旋转，或磁通门，这是一种特殊类型的线圈。有些人用天平或弹簧来测量另一个磁铁所受的力——有时用显微镜。你甚至可以利用克尔效应或法拉第旋转等光学特性来探测磁场。

然后你进入真正奇异的传感器。您还可以测量煤油等富氢材料中的质子共振，或者检测铯等气体中的能量状态。超导线圈也在菜单上。

然而，霍尔效应，尤其是使用半导体的霍尔效应，既便宜又丰富。它们也很小。很难想象你的电脑键盘会使用超导线圈来吸附粘在按键底部的小磁铁。

## 它是如何工作的？

我们喜欢来自[rcmodelreviews]的视频，它讲述了霍尔效应背后的理论(见下文)。然而，即使没有视频，解释也很简单。考虑形状像一美元钞票的导电片。连接在左右两侧的是一个恒压源，使电流流过导体。如果你测量钞票上下两端的电压——霍尔电压，如果导体良好，你会认为电压接近于零。如果没有磁场，你可能是对的。顶部和底部之间的电压实际上为零伏。

然而，当磁场中的磁力线与偏置电流成直角时，洛伦兹力会作用于电子或其他电荷载体，如空穴，它们会弯曲远离该力，如您在该动画中所见。这将导致电子在导体的一侧聚集在一起，而在另一侧则趋于消失。

 <https://hackaday.com/wp-content/uploads/2021/03/Hall_Sensor.webm?_=1>

[https://hackaday.com/wp-content/uploads/2021/03/Hall_Sensor.webm](https://hackaday.com/wp-content/uploads/2021/03/Hall_Sensor.webm)

霍尔效应动画由【FraunhoferIIS】， [CC-BY-SA-4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.en) 制作。

这导致两边带不同的电荷，有电荷差的地方，就一定有电压。在动画中，您可以看到，当马蹄形磁铁向设备施加不同的磁场时，电池提供电流，电表测量霍尔效应电压。

 [https://www.youtube.com/embed/QMsuv9PadpY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QMsuv9PadpY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



一个实用的设备将有额外的电路。通常，霍尔电压有一个放大器。有时有一个偏置电压调节器。数字输出传感器也可以有一个比较器和一个输出晶体管。

## 阅读数据手册

每个器件都是不同的，因此阅读您想要使用的器件的[数据手册](https://mel-prd-cdn.azureedge.net/-/media/files/documents/datasheets/mlx91208-datasheet-melexis.pdf)是有好处的。霍尔效应通常对频率范围有限制，并且可能相当昂贵。例如，Melexis 有一个 250 kHz 的设备，比许多其他类似产品快得多。该特定器件的工作电压为 5 V，电流小于 15 mA。

从数据手册中，您可以看到有两个版本。一个可以工作到大约 7.5 毫特斯拉，另一个工作在大约 20 毫特斯拉。甚至有一个版本可以工作到 60 毫特斯拉。当然，其他供应商也有许多不同参数的选择。

 [https://www.youtube.com/embed/DKdehe1BzYo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DKdehe1BzYo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



一些传感器输出与感应磁场成比例的电压，或者你可以得到一个数字开/关型传感器。显然，如果您希望部署一个传感器，那么无论您选择使用哪个传感器，都需要不同的支持。在某些情况下，你甚至不需要外部设备。例如，ESP32 内置了自己的霍尔效应，正如您在该视频中看到的那样。

## 带有霍尔效应传感器的建筑物

如果你想建立自己的霍尔效应项目，有很多可供选择。一个[便携式磁力计](https://hackaday.com/2020/01/24/feel-the-force-with-a-pocket-magnetometer/)相当简单，装在一个 Tic Tac 盒子里。如果你正在[测量电流](https://hackaday.com/2018/08/24/tracking-the-office-coffee-machines-using-current-draw/)，你可能想要使用一个不仅包含霍尔效应传感器，还包含你需要的其他一切的设备。

或者，为什么不造点新的？不过，如果你这样做了，一定要在提示热线上给我们[发一条短信，这样我们就可以传播你的最新创作了。](https://hackaday.com/submit-a-tip/)