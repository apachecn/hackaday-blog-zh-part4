# 为速度快的工人准备的焊接光剑

> 原文：<https://hackaday.com/2020/03/28/a-soldering-lightsaber-for-the-speedy-worker/>

说到烙铁，我们都有自己的偏好，而对[Marius tac iuc来说，最强的是快速加热。在他去上班的时间里，它必须处于最高温度，否则它根本不能满足要求。[他的解决方案是温控熨斗，但是没有普通温控](https://hackaday.io/project/170204-soldering-lightsaber)。它使用机器学习算法来寻找最快的预热，而不是普通的反馈回路。

他使用的元件有一个与元件本身串联的热电偶，这意味着为了测量温度，必须切断元件的电源。这个占空比不能切得太短，否则测量会变得有噪声，因此在传统的温度控制制度下，加热的速度是有限制的。他的方法是在一段时间内不停地打开它来测量温度，只有在它有机会变热后才进行测量。该算法不断学习多长时间打开它以达到什么温度，并能够进行插值以达到所需的读数。这是一种让现有硬件表演新把戏的聪明方法，我们喜欢这样。

这些年来，他在这些页面上出现了好几次，但也许你想看看相同硬件的第一个版本。与此同时，观看快速升温的过程，并在下面的视频中进行更全面的解释。

 [https://www.youtube.com/embed/q1-CvRvSn28?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/q1-CvRvSn28?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

