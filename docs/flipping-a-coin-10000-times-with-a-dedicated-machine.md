# 用专用机器将硬币翻转 10000 次

> 原文：<https://hackaday.com/2020/07/21/flipping-a-coin-10000-times-with-a-dedicated-machine/>

抛硬币通常是帮助数学学生学习概率和统计的最初例子。人们经常谈论，给定一枚公平的硬币，正面或反面落地的概率应该接近 0.5。当然，如果你想测试这个，让一台机器为你做艰苦的工作是值得的。安德鲁·康斯洛有能力做到这一点。

该建筑主要由 3D 打印部件组成。一个大的圆柱形护罩用于将硬币保持在翻转区域内。一个装有弹簧的销钉由一个旋转凸轮的步进电机驱动，从而翻转硬币。一旦硬币落地，就会被摄像头拍摄下来。然后，图像处理管道确定硬币落下时是正面还是反面。硬币的一面有一个黑点用于帮助分析，因为低质量的网络摄像头图像不足以识别标准形式的硬币。一旦翻转被分析，一个滑动孔被用于将硬币推回翻转装置，用于下一个循环。

机器大约每两秒完成一次翻转，这意味着 10，000 次翻转大约需要 2.5 天。不幸的是，由于噪音和偶尔的硬币逃逸，[安德鲁]还没有能够实现他的目标。他的目标是在全力以赴之前大幅提高速度。

抛硬币可以得到不错的随机数，但是如果你需要更好的，也许 NIST 可以帮你。休息后的视频。

 [https://www.youtube.com/embed/R4jDcv085Hw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/R4jDcv085Hw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

