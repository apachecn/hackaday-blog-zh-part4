# 地板上的四个是你的虚拟赛车

> 原文：<https://hackaday.com/2020/07/17/four-on-the-floor-for-your-virtual-race-car/>

曾经有一段时间，建造逼真的车辆模拟是美国宇航局和大公司的事情。今天，许多人拥有复杂的虚拟驾驶舱或赛车，他们使用高分辨率屏幕甚至虚拟现实设备。如果你仔细想想，虚拟汽车并不难实现。你真正需要的只是一个方向盘、几个踏板和一个换挡杆。当然，你可以建造风扇来模拟风，并在你的座位上放置触觉设备，但实际上输入设备本身就能让你实现大部分目标。[Oli]决定他想要一个快速简单的[USB 换挡器](https://www.olinorwell.com/how-to-build-a-usb-gear-stick-h-shifter/),所以他去了趟五金店，拿起一个街机操纵杆，然后用 Arduino Leonardo 把它们绑在一起。你可以在下面的视频中看到的成品花费了大约 30 美元，花费了不到 6 个小时的时间来制作。

当然，莱昂纳多有能力像 USB 人机接口设备(HID)一样工作，所以它可以模仿鼠标、键盘或操纵杆。正如您所料，这对这个项目来说很方便。计算机只需读取四个操纵杆按钮，然后决定哪个档位匹配哪个按钮。例如，向左上方是第一档，而第四档只是按下向下按钮。一个定制的木制换档板给你一个典型的 H 型模式，你期望从一个坚持转变。

当然，操纵杆不像真正的手动档那样有很长的手柄，所以[Oli]增加了一些扩展。此外，一个真正的换挡器不需要你像操纵杆一样把它保持在适当的位置。为了纠正这一点，换档板有磁铁抓住并保持它。它们不够强壮，以至于你不能移动棍子，但是它们足够强壮，以至于它不能自己移动。

我们注意到这个设计没有考虑到离合器，所以这和驾驶一个真正的手动挡不太一样。然而，[奥利]提到了几个他心目中的升级，离合器是其中之一。一些触觉将是一个很酷的附加功能，所以如果你没有正确换档，你可以感觉到齿轮在摩擦。

我们看到的最后一个这样的[换挡器](https://hackaday.com/2020/01/08/3d-printable-stick-shift-for-your-racing-simulator/)是 3D 打印的。在美国越来越难找到手动挡的车，但[克里斯蒂娜·帕诺斯]绝对是[的粉丝](https://hackaday.com/2020/05/05/sticking-up-for-the-stick-shift/)。

 [https://www.youtube.com/embed/lWDyUr7-dn4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lWDyUr7-dn4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

