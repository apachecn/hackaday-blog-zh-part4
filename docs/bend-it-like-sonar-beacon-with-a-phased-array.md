# 用相控阵弯曲它像(声纳)信标

> 原文：<https://hackaday.com/2022/02/23/bend-it-like-sonar-beacon-with-a-phased-array/>

超声波传感器是不可思议的，有了它们，你可以探测距离，也可以悬浮和窥视物体。它们可以发射和接收超声波(通常在 18khz 以上)，就像所有的波一样，它们可以通过相控阵来控制。[Bitluni]试图精确测量距离，但发现传感器的大视野太不精确，所以他[制作了一个相控阵传感器](https://www.youtube.com/watch?v=z4uxC7ISd-c)。

灵感来自于【2019 年关于相控阵的 Hackaday Supercon 演讲。[Bitluni]通过一个出色的解释，讲述了阵列如何与一桶水和他的手指一起工作，以及一个单独的模拟。通过改变不同阵列成员的相位偏移，可以有效地控制波束，因为干扰屏蔽了不需要的波。利用一组螺线管，他创建了一个测试平台，在他能看到的介质中验证他的想法；水。螺线管向水中发射一个脉冲，产生一个波。你可以看到波浪在水中朝着正确的方向运动，这验证了这个概念。一个简单的 PCB 被送到一个带有模板的工厂，提供了一个焊接传感器和驱动器的表面。ESP32 驱动 8 个 PWM 信号，这些信号进入发射器，并通过一个小放大器读入单个接收器。他仍然不满足于让这个想法被证实，他在他的 CNC 机架上设置了接收器，并绘制了不同点的信号强度，产生了美丽的“热图”


它以大约每秒 1-3 帧的速度扫过前方 60 度的区域。正如你可能想象的那样，将声波反射转换成距离场是一件有些嘈杂的事情。他将声纳显示器投射到我们在相机中所能看到的顶部，看到斑点在正确的位置排成一行是很有趣的。

我们注意到他建造了相当多的电路板，也许在将来，他会像这个 100 传感器阵列一样按比例放大？休息后的视频。

 [https://www.youtube.com/embed/z4uxC7ISd-c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/z4uxC7ISd-c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

