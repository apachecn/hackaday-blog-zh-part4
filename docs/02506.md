# 廉价烤面包机的惊人技术

> 原文：<https://hackaday.com/2019/03/27/the-surprising-tech-of-a-cheap-toaster/>

烤面包机能有多复杂？你可以用不到 10 美元买到一个便宜的，比热线稍微多一点的。然而，有一些小的并发症。首先，消费品需要安全——诉讼费用昂贵。第二，必须有某种机制来压制吐司，直到它完成。如果你能花 10 美元买一个，你可以打赌它不是运行 Linux 的超级吐司处理器。

【科技连线】[给你拆了一个](https://www.youtube.com/watch?v=zLFG068HtgM)这样你就不用。电路很简单，谁知道有一个控制烤面包机的专用集成电路？然而，真正的工程是在你拉下小把手开始敬酒的时候。

这个小小的机械装置就像一个电源开关，一个电路断路器，在烤面包准备好之前把它压下去。杠杆接通电源，从而启动电磁铁。当烤面包机决定完成时，它会关闭磁铁，磁铁不仅会弹出面包片，还会关闭整个烤面包机。这很简单，但也不太简单——正如我们常说的，少并不是真的多；适可而止。

平心而论，里面的 IC 只不过是一个集成的 555 定时器。暗度控制设置频率(标称值为 1024 Hz ),定时器维持输出，直到定时器超时。当然，这是最便宜的烤面包机了。有些烤面包机非常别致，有实时计时器、温度或颜色传感器，有些甚至可以在烤面包上打印天气预报。在这篇[恩智浦应用笔记](https://www.nxp.com/docs/en/application-note/AN3414.pdf)中，您可以一窥更复杂的烤箱。

未来的烤面包机可能有他们自己的神经官能症。你甚至可以拥有[一个飞行烤面包机](https://hackaday.com/2013/11/13/flying-rc-toaster/)，但是我们不知道为什么。有了你自己的烤面包机，你再也不用为早餐没有烤面包而苦恼了——如果你不能忍受烤面包，这很有帮助。

 [https://www.youtube.com/embed/zLFG068HtgM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zLFG068HtgM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

