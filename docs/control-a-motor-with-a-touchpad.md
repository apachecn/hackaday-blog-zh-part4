# 用触摸板控制电机

> 原文：<https://hackaday.com/2020/06/10/control-a-motor-with-a-touchpad/>

旧笔记本电脑内部有数量惊人的部件，可以很容易地清理掉，但通常这些电子产品的专有信息需要大量的工作才能使它们再次有用。显然，硬盘和内存等东西可以很容易地再次使用，但也有可能通过一些努力让屏幕或电池等东西与其他设备一起工作。[现在，还有一种方法可以重复使用触控板](https://www.instructables.com/id/Reuse-Old-Laptops-Touchpad-to-Control-a-Stepper-Mo/)。

这个版本使用了一个内置 Synaptics 芯片的 PS/2 触摸板，在触摸板上焊接几个引脚后，它可以非常顺利地与 Arduino 集成。大多数工作都是在触摸板的内置芯片上完成的，因此一旦 Arduino 接收到触摸板的输入，它就可以自由地用它做几乎任何事情。在这种情况下，[Kushagra]在一些不同的实现中使用它来操作步进电机。

如果你有这种类型的触摸板，所有的代码和图表都可以在项目页面上找到。零件箱中的旧笔记本电脑肯定会有很多用途，即使在你[取下屏幕](https://hackaday.com/2019/03/14/an-hdmi-input-for-laptop-screen-minus-laptop/)之后，但不要忘记你 1995 年的旧[米色 PS/2 鼠标肯定也会有这样的一些用途。](https://hackaday.com/2008/05/16/how-to-scavenge-a-mouse-for-parts/)

 [https://www.youtube.com/embed/3z0P9IMHIpU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3z0P9IMHIpU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

