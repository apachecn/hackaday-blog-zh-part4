# Arduino 为数字检测范围提供了免提对焦

> 原文：<https://hackaday.com/2018/11/12/arduino-provides-hands-free-focus-for-digital-inspection-scope/>

随着表面贴装技术将元件尺寸推得越来越小，即使是我们当中最敏锐的人也需要某种光学辅助来完成 PCB 工作。很多显微镜也有数码相机，这是一个很大的帮助——除非相机和你打架。

面对一台自动对焦目标的想法与他的想法不太一致的相机，[斯科特·m·贝克]亲自动手——实际上是用脚——用外置控制器取代了鼠标对相机的输入。他的特定相机的自动对焦可以关闭，但只能通过鼠标点击相机的 GUI。这在焊接时会造成干扰，因此[Scott]使用 Arduino Pro Micro 和一个小键盘来模拟控制摄像头所需的鼠标移动。

按下一个键，Arduino 会将鼠标光标移到屏幕的左上角，下拉相机菜单，并向下移动适当的距离来切换自动对焦。控制器还可以运行手动对焦或截图。甚至还有一个脚踏开关，如果视野发生变化，它会迫使相机重新聚焦。它看起来真的很方便，像往常一样[Scott]在下面的视频中提供了一个很好的演示。

不管你喜不喜欢，如果缩小技术不强迫你进入显微镜市场，[熵就会](http://hackaday.com/2016/06/22/a-hackers-guide-to-getting-old/)。如果你正在寻找一份显微镜的购买指南，你可能会比[【沙里尔】的数字 USB 示波器的综述](https://hackaday.com/2017/11/14/if-you-want-to-spend-on-a-microscope/)更糟糕。或者也许你更喜欢在[的垃圾箱里翻找你的](https://hackaday.com/2014/08/02/finding-and-repairing-microscopes-from-the-trash/)。

 [https://www.youtube.com/embed/47TUqyfH6N4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/47TUqyfH6N4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

