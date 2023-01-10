# 虚拟现实手套旨在提高互动性

> 原文：<https://hackaday.com/2021/04/15/virtual-reality-gloves-aim-to-improve-interactivity/>

虚拟现实在某些方面是一个发展缓慢的领域。虽然很多焦点都放在光学技术和耳机上，但当涉及到将一个人可信地置于虚拟环境中时，还涉及到更多的东西。到目前为止，我们在视觉和头部跟踪方面有了一个良好的开端，但交互技术仍然落后很多。[【卢卡斯】正在那个领域工作，在他自制的虚拟现实手套](https://www.youtube.com/watch?v=nmP8iGaPbeI)上不断重复。

这种手套由电位计组成，配有线轴，通过一根绳子连接到佩戴者手上的每个手指头上。当用户弯曲手指时，电位计转动，可以测量手指的位置。电位计都通过 Arduino 读取，Arduino 通过 USB 与 PC 通信。然后使用自定义驱动程序与 Valve 的 SteamVR 软件进行交互，从而允许手套与各种现有软件配合使用。

到目前为止，该系统只是跟踪手指的位置，但基于线轴和线的设计旨在支持每个手指的电机，以产生阻力，因此用户可以获得触摸虚拟物体并与之互动的感觉。该项目有可能成为比目前现成的解决方案更便宜、更容易获得的替代方案。[我们以前也见过其他追踪手的手套](https://hackaday.com/2019/10/25/haptic-glove-controls-robot-hand-wirelessly/)——尽管没有一种能追踪佩戴者的手的伸展和手指的伸展。如果你正致力于此，[请给我们写信。](http://hackaday.com/submit-a-tip)休息后的视频。

 [https://www.youtube.com/embed/nmP8iGaPbeI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nmP8iGaPbeI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

