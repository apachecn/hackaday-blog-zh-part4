# 港口货运发动机上的 Hypercar 阀门技术

> 原文：<https://hackaday.com/2020/12/17/hypercar-valve-technology-on-a-harbour-freight-engine/>

活塞发动机的进气门和排气门正时对发动机性能起着很大的作用。许多现代汽车发动机具有某种可变气门正时，但是气门仍然机械地连接在一起并连接到曲轴。这意味着各种工作条件下总会有一定程度的性能折衷。[Wesley Kagan]从 Koenigsegg 的无凸轮自由阀技术中获得灵感，[将港口货运发动机转换为无凸轮技术，用于单独的阀门控制](https://www.youtube.com/watch?v=k_MrPylnsDg)。

通过取消传统的凸轮轴，并为每个气门提供其致动器，可以针对任何特定的工作条件甚至每个气缸调整气门正时。廉价的单缸发动机是车库黑客的完美测试平台。[Wesley]移除了摇臂和推杆，并用 3D 打印的摇臂盖替换了普通摇臂盖，该摇臂盖包含两个推动弹簧气门杆的小型气动活塞。这些活塞由高速气动电磁阀控制。曲轴仍然需要参考正时信号，因此[Wesley]建立了一个带有 3D 打印正时轮的正时系统，该正时轮包含一堆嵌入的磁体，并由固定的霍尔效应传感器感测。Arduino 用于读取正时轮位置并将控制信号输出到电磁阀。通过一个粗略的计时程序，他能够让发动机运转起来，尽管它无法加速。

在休息后的第二个视频中，他制作了发动机现有凸轮轴的数字副本。利用 3D 打印支架中的两个电位计，他测量了完整发动机循环的推杆运动。他仍然计划为每个阀门增加位置感应，在对单缸发动机做了更多的工作后，他计划改装一辆全尺寸汽车，这是我们所期待的。

自从有了汽车，人们就一直在车库里摆弄汽车。[Lewin Day]一直在做一个关于如何自己动手修理汽车的系列报道。随着现代汽车中所有的电子设备，[摆弄他们的软件](https://hackaday.com/2020/12/10/remoticon-video-learn-how-to-hack-a-car-with-amith-reddy/)已经成为这种古老的消遣方式中日益增长的一部分。

 [https://www.youtube.com/embed/k_MrPylnsDg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/k_MrPylnsDg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/z-RR0AJyTq8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/z-RR0AJyTq8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

