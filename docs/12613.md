# 无线电控制作业飞机使用六个倾转旋翼飞行

> 原文：<https://hackaday.com/2022/01/29/radio-control-joby-aircraft-uses-six-tiltrotors-to-fly/>

电动垂直起降(电动垂直起降)飞行器是最近开发的一些更令人兴奋的飞行器。他们旨在将直升机的机动性和着陆优势与电力驱动的环境优势结合起来，并经常被吹捧为空中出租车实用的唯一方式。Joby Aviation 的飞机是该领域最先进的，彼得·雷塞克着手建造一个无线电控制的模型，以同样的方式飞行。

![](img/6c3a5582a72b37c6dee204d18ad041dc.png)

The design is inspired by the Joby eVTOL test vehicle.

结果是非常复杂的，六个倾斜的旋翼通过伺服系统控制以获得最大的机动性。这些允许车辆垂直起飞，同时允许旋翼水平倾斜，以提高向前飞行的效率，正如在[贝尔-波音 V-22 鱼鹰上看到的那样。](https://en.wikipedia.org/wiki/Bell_Boeing_V-22_Osprey)

该建筑使用 3D 打印的底盘，尽可能简单地实现所有的倾斜旋翼安装和机制。一个小小的飞行控制器负责控制飞行器，运行 [dRehmFlight VTOL 固件。](https://github.com/nickrehm/dRehmFlight)组装好的飞行器包括电池在内仅重 320 克；相对于常规的四轴飞行器，这是一个令人印象深刻的成就。

经过一些调整，悬停飞行被证明相对容易实现。在这种模式下，内部的四个马达像传统的四轴飞行器一样使用，不断改变转速以保持飞行器稳定。然后，外部的两个马达根据需要转动，以获得额外的控制权限。

在向前飞行时，通过调节中央四个马达的角度来控制俯仰。滚转是通过倾斜飞机中心轴两侧的旋翼实现的，偏航控制是由差动推力提供的。在模式之间的过渡期间，在两种模式之间使用简单的插值，直到过渡完成。

室外飞行测试表明，该飞行器很容易像传统的固定翼飞机一样优雅地向前飞行。在悬停模式下，它看起来就像任何其他多旋翼飞机。总的来说，这是建造一艘成功的倾转旋翼机的一个很好的示范。

[我们在](https://hackaday.com/2018/11/06/tilt-rotor-plane-needs-flight-controller-hack-to-get-airborne/)之前已经见过倾转旋翼无人机，它们很酷，因为它们建造起来很复杂。休息后的视频。

 [https://www.youtube.com/embed/Dd2N_lyO_SQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Dd2N_lyO_SQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

