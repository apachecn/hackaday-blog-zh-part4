# 使用这款物联网卷纸架记录卫生纸的使用情况

> 原文：<https://hackaday.com/2022/02/03/keep-track-of-toilet-paper-usage-with-this-iot-roll-holder/>

还记得 2020 年的卫生纸大危机吗？我们确实如此，看起来我们的老朋友[Vije Miller]也是如此，同时似乎对每个上厕所的人消耗多少纸张怀有某种病态的迷恋。为此，我们展示了[他的物联网卫生纸追踪器](http://vijemiller.com/index.php?t=NodeMCU_WiFi_Toilet_Paper_Sheet_Counter)。

他的 3D 打印卷筒固定器有一个霍尔效应传感器，可以计算卷筒的转数，并将其发送到 NodeMCU。每卷纸的数量是在换辊时输入的，因此一些简单的数学计算就可以得出每个美国佬消耗的纸的数量。或者至少是一个合理的估计——[Vije]承认有必要进行一些四舍五入。这个构建最好的部分是与 Thingspeak 的连接，在这里可以绘制和显示工作表的使用情况。有本事就去看看；在撰写本文时，纸张使用量出现了惊人的峰值——突然需要 68 张，而基线使用量是个位数。我们不敢想象是什么促成了这一切。下面的视频是——好吧，就说有视频吧。

这不是我们第一次看到[Vije Miller]基于浴室的项目。几年前，有人试图用等离子体清新空气，T2 的物联网淋浴阀门控制器可能从未意外烫伤过任何人。

 [https://www.youtube.com/embed/JLKftQCVsK8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JLKftQCVsK8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Fiona Grutza]的提示。

[通过 [r/arduino](https://www.reddit.com/r/arduino/comments/sipk50/wifi_enabled_toilet_paper_sheet_counter_to_track/)