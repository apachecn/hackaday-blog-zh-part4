# 显而易见的技术:雨量感应雨刷

> 原文：<https://hackaday.com/2022/08/25/tech-in-plain-sight-rain-sensing-wipers/>

当开始下雨时，你不想手动打开挡风玻璃雨刷，这绝对是一个第一世界的问题，但这也是那些听起来比实际容易解决的事情之一。毕竟，你可以问一个四岁的孩子是否在下雨，并期待一个合理的答案。但是你怎么问计算机这个问题呢？尤其是一台几乎完全靠自己运行的小型廉价电脑。

你可能想在这里停下来，试着想想你会怎么做。测量玻璃的电导率？也许玻璃上的水影响了它的介电常数，你可以测量由此产生的电容？现代汽车两者都没有。这个问题很复杂，因为你需要一个与玻璃兼容的解决方案，并且不容易因为灰尘或碎片而出现假阳性。

[![](img/e6810f059af0a377fd77fc7f96b7e258.png)](https://hackaday.com/wp-content/uploads/2022/08/wipe.jpg)

Source: [https://cecas.clemson.edu/cvel/auto/systems/wiper_control.html](https://cecas.clemson.edu/cvel/auto/systems/wiper_control.html)

取而代之的是，他们用红外线以一个角度射向挡风玻璃。玻璃将大部分光线反射回传感器，但水会导致反射光散射。如果传感器看到较少的返回光，它会打开雨刷。传感器在哪里？这取决于汽车，但[Jeff]在下面的视频中指出了丰田汽车上的位置。

通常，整个组件位于挡风玻璃后面靠近后视镜的地方。在克莱姆森汽车电子实验室网站上有一篇很好的文章和图片。

当然，汽车公司并不是从零开始设计的。他们从其他公司购买技术，例如，[滨松](https://www.hamamatsu.com/us/en/applications/automotive/automatic-wiper.html)和其他公司。

 [https://www.youtube.com/embed/qZWIyUandqA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qZWIyUandqA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



曾经有一段时间，如果你不能忍受手动操作你的雨刷，你可以购买[套件](https://rainsensors.com/2015/11/10/rt/)来添加到你的汽车上。如果你愿意的话，自己动手应该不会太难。

当然，同样的事情也有其他的方法。一些特斯拉汽车可以用它们的摄像头被动地探测降雨。此外，如果你不需要感知玻璃，测量变湿对 [PCB 电阻器](https://www.electroduino.com/rain-sensor-module-how-its-works/)的影响是非常容易的。

令人惊讶的是，有多少事情对人类来说很容易理解，但对计算机来说却困难得多。虽然我们确实喜欢我们的自动雨刷，但我们也不介意在必要时打开它们。我们偶尔也会得到假阳性。

挡风玻璃雨刷背后的技术[数量惊人。更不用说，潜在的，](https://hackaday.com/2020/04/23/the-back-and-forth-of-windshield-wipers-and-patent-lawsuits/)[节奏](https://hackaday.com/2022/03/31/making-windshield-wipers-rock-to-the-beat/)。

横幅图片:Basheer Tome 的作品:[Rain Rain Go](https://www.flickr.com/photos/10019047@N05/4597461278)。Wonderlane 的:“[美国银行连续提款机，挡风玻璃雨刷，雨，美国华盛顿州西雅图大学村](https://www.flickr.com/photos/71401718@N00/5245301952)”。