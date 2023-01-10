# 家酿卷绕机使圆环卷起来很容易

> 原文：<https://hackaday.com/2020/06/05/homebrew-coil-winder-makes-toroids-a-snap-to-wind/>

任何曾经手工绕过环形线圈的人都会告诉你，这并不是一件有趣的工作。即使是业余无线电的扼流圈和变压器中使用的那种线圈，通常只有相对较少的绕组，将所有的电线一次又一次地穿过环形线圈也是一件痛苦的事情。谁要是猜错了这项工作需要多少电线，谁就倒霉了。

为了解决这些问题，【Sandeep】想出了[这个聪明而有效的环形绕线机](https://electricdiylab.com/diy-arduiuno-based-toroid-coil-winding-machine/)。这个想法是通过一个小线轴的磁线通过圆环的核心，同时旋转圆环，以尽可能均匀地展开绕组。这显然需要一个可以打开的缠绕环，以允许插入环形线圈；[Sandeep]选择用胶合板做他的缠绕环，上面有一条缝。带着线轴，缠绕环在 C 形夹具上旋转，夹具支撑着圆环，圆环本身在步进电机的控制下在三个滚轮上旋转。Arduino 控制两个电机的旋转，控制绕组的数量及其在表单上的分布。由于缺乏测试用的铁氧体磁芯，[Sandeep]使用了一个胶合板环作为替代品，但结果令人满意，足以让任何手动绕线机羡慕不已。

我们喜欢这样的工具，它让枯燥的工作变得轻而易举。无论是[切割线束的电线](https://hackaday.com/2017/10/28/automate-wire-prep-with-a-robot-wire-cutter/)还是[缠绕吉他拾音器](https://hackaday.com/2016/06/18/cnc-upgrade-to-guitar-pickup-winding-machine/)，像这样的工具非常值得花时间来制作它们。但我们认为，当谈到环形绕组，[一个人总是可以欺骗](https://hackaday.com/2013/02/13/toroid-winding-cheat/)。

 [https://www.youtube.com/embed/46rbpPwqelY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/46rbpPwqelY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[通过 [r/Arduino](https://www.reddit.com/r/arduino/comments/gtynju/diy_arduiuno_based_toroid_coil_winding_machine)