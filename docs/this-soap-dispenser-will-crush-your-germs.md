# 这个皂液器会消灭你的细菌

> 原文：<https://hackaday.com/2020/07/17/this-soap-dispenser-will-crush-your-germs/>

说到洗手，[Arnov Sharma]可不是闹着玩的。他使用超声波传感器、启动泵的步进电机和容纳一瓶肥皂的 3D 打印组件建造了一个自动皂液分配器，这是过度工程的壮观展示。至少他不需要在超市排队买运动检测皂液器了。

最初，他的想法是用一种普通的基于伺服电机的方法来制造分配器。这将涉及到启动马达以向下推动肥皂瓶的活塞来分配肥皂。相反，他提出了一种不同的方法，这种方法在理论上相当简单，尽管执行起来相当复杂。

![](img/928abe950471d66ca9cf7a41ec378d44.png)

Model of the soap dispenser made in Fusion 360

他首先通过 3D 打印肥皂瓶放置的隔间和向下推动肥皂瓶的 Z 轴导轨的结构支撑。这类似于 3D 打印机或 PCB 工厂中的线性致动器类型，其中电机控制旋转螺杆，使托架在皮带上移动。(我们假设线性轨道最先出现，然后是超声波皂液器。)

在这种结构中，增加了两个额外的杆来帮助支撑压在皂液器上的杠杆。

该设置由 Arduino 控制，如果收到来自超声波传感器的信号，就会触发线性致动器的运动。他添加了模型文件和 Arduino 代码，供其他对构建类似项目感兴趣的开发者使用。看看他的皂液器的视频——步进电机绝对会比你想象的更有力。

 [https://www.youtube.com/embed/Pi4bStBNVAo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Pi4bStBNVAo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2020](https://prize.supplyframe.com) is Sponsored by:[![Supplyframe](img/193ca31946d20fcfa39296cb816a4c50.png)](https://supplyframe.com/)[![Digi-Key](img/4fc24a8a6b4498aecfe987b00009d192.png)](https://www.digikey.com/)[![Microchip](img/8dd361210bbb0e5592c24f87e4e2267e.png)](https://www.microchip.com/)[![Arm](img/7d728b281b85469ef9013d45001f14b4.png)](https://www.arm.com/)