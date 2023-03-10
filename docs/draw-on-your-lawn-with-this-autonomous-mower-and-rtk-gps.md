# 用这台自动割草机和 RTK-GPS 在你的草坪上画画

> 原文：<https://hackaday.com/2020/08/16/draw-on-your-lawn-with-this-autonomous-mower-and-rtk-gps/>

开源硬件的兴起已经见证了各种各样费力的任务成功地自动化，为我们人类节省了大量的麻烦。可以说，有些家务比其他的更容易自动化。以无害的自主真空吸尘器的经典案例为例，它可能非常笨，在这个地方颠簸，以预编程的清扫模式盲目地穿过房间，以检测周边。

原则上，这个想法可以延伸到修剪你的草坪。但是，你真的想要一个高速旋转的刀片猖獗，因为它漫无目的地冒险在你的草坪外？Ardumower 自动割草机项目的 Sunray 更新解决了这个问题，而无需铺设实际的周界电线。由于标准的消费级 GPS 不够精确，因此解决方案包括实施您自己的 RTK-GPS 硬件和一个配套的基站，为您的割草工作带来厘米级的精度。

RTK-GPS，也称为载波相位增强 GPS，通过使用位置已知准确的参考接收器测量信号中的误差来提高标准 GPS 的精度。这些信息随后通过无线电线路传递给 Ardumower 板，这样它就可以相应地调整自己的位置。你需要在你的草坪上雕刻表情符号的能力吗？不。但你还是可以拥有它。如果这还不足以让[开始自主割草机革命](https://hackaday.com/2017/03/01/where-are-the-autonomous-lawnmowers/)，我们不知道什么才是。

 [https://www.youtube.com/embed/SU-_ZQzKm3E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SU-_ZQzKm3E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

