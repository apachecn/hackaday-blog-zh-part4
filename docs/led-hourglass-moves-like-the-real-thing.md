# LED 沙漏像真的一样移动

> 原文：<https://hackaday.com/2021/01/27/led-hourglass-moves-like-the-real-thing/>

如果你想有意义地浪费时间，给自己买一个沙漏。坐在那里，看着时间一秒一秒地溜走，这既令人着迷又令人害怕，因为这是区分可能性和错失机会的门槛。

[![](img/feec549b354f2422839fcb1f6b24e03a.png)](https://hackaday.com/wp-content/uploads/2021/01/hourglass-animation.gif)[【Ty and Gig】的 LED 沙漏看着](https://www.instructables.com/LED-Hour-Glass/)也一样美。它实际上并不显示时间，但这对我们来说完全没问题。不管沙漏如何倾斜，它所做的就是让 led 产生动画效果，以模拟重力作用下的沙粒。

在任一垂直方向，只要顶部有沙子，沙子就会落下。当沙漏水平放置时，发光二极管就像真正的沙子一样稳定下来。【Ty 和 Gig】用[大量的代码](https://github.com/tmckay1/led_hour_glass/blob/main/hour_glass_2.ino)实现了这一点，这些代码将动画帧分解成结构数组。

相比之下，这个构建的硬件部分相当简单:复制这个构建所需要的只是一些 RGB LEDs、驱动它们的强大电源、加速度计和微控制器。

[Ty 和 Gig]计划使用 ESP8266，但放错了地方，转而使用 Arduino Mega。(你知道他们怎么说——买一个替代品，你丢失的那个几乎马上就会出现。)这个漂亮的框架是由剩余的紫心木制成的，紫心木是一种暴露在空气中会变成紫色的硬木。休息之后，请观看构建视频。

懒得每小时重置一次沙漏？这里有一个会自己翻转的。

 [https://www.youtube.com/embed/yeIhOZMU5To?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yeIhOZMU5To?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

