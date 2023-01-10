# 电机驱动运动使 POV 玩具现代化

> 原文：<https://hackaday.com/2021/02/24/motor-driven-movement-modernizes-pov-toy/>

正如我们今天被迫观看每一次循环都变得更好的 gif 一样，100 多年前的人们用各种视觉暂留玩具自娱自乐，这些玩具利用视错觉的力量使静止图像变得栩栩如生。[【jolly factory】最近将第一批 POV 设备之一](https://www.instructables.com/A-Modern-Take-on-the-Phenakistoscope/) —幻灯机(phenakistoscope)改造成了我们这个时代的玩具。

最初的幻灯机很简单，但它们所达到的效果却非常惊人。本质上是一个带手柄的图片盘，用户可以用一只手握住手柄，用另一只手旋转图片盘，同时通过图片盘上的狭缝看镜子。不像以前的幻灯机一次只能由一个人观看，这个允许集体观看。

它是这样工作的:一个 Arduino Nano 从一个旧的 CD-ROM 驱动器旋转一个 BLDC 马达，两条频闪 led 提供了使图片看起来像移动图像所需的快门效果。电机速度既可变又可逆，因此动画可以在两个方向上运行。

为了自己制作光盘，[jollifactory]打印了一些原始的幻视艺术作品，并将每张光盘粘贴在一张 CD 上，这张 CD 可以方便地卡在电机主轴上。并不是所有的艺术品中间有一个大洞看起来都很好，所以[jollifactory]创造了一个可重复使用的底盘，顶部有防滑垫来旋转这些艺术品。

如果你只是想看看这个东西的运行，看看下面的第一个视频，这是所有的演示。前方有闪光灯，所以你要小心。第二个和第三个视频显示[jollifactory]焊接定制的 PCB 并构建丙烯酸支架。

有很多现代方法来制造老式的 POV 玩具，从[全数字](https://hackaday.com/2016/03/11/digital-zoetrope-powered-by-pi/)到[全打印](https://hackaday.com/2016/06/29/3d-printed-zoetrope-sculpture-squashes-4-dimensions-into-3/)。

 [https://www.youtube.com/embed/SDfcNgCvIVg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SDfcNgCvIVg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/EUEtSydIHUI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EUEtSydIHUI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/ugPOK2VlTaA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ugPOK2VlTaA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

