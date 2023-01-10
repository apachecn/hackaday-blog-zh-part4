# 花费最少的睡眠监视器

> 原文：<https://hackaday.com/2022/06/15/a-sleep-monitor-for-minimum-outlay/>

睡眠研究中使用了多种仪器来测量睡眠期间的身体活动以及随之而来的睡眠质量。他们中的许多人使用的技术可能不太容易在工作台上复制，但使用现成的模块可以实现 EEG 或脑电图仪来测量脑电波。[ 本·贾比图亚 ]向我们[展示了一个使用这些模块中的一个](https://www.majorinput.co.uk/post/arduino-based-eeg-sleep-monitoring)、一个蛋 Mikroe Click 的睡眠监视器。

该手术的大脑是一个阿达果阿达洛奇羽毛 M0，它被连接到一个包含传感电极的头带上。这篇文章给了我们一个可用电路板的汇总，这对这个领域的任何实验者来说都应该是方便的。同时，固件是使用 Arduino IDE 编写的。它将原始采样数据收集到 SD 卡中，令人惊讶的是，存储一夜的结果只需要相对较小的空间。

最后，使用 Python 脚本来处理数据，并将其转换为光谱图，以观察夜间的大脑活动。他设想在快速眼动睡眠期间使用该装置来触发清醒梦，但我们可以看到它可能对睡眠障碍患者也相当有用。在休息下面的视频里看一下。

 [https://www.youtube.com/embed/J7UTS3hUacw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/J7UTS3hUacw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

