# 瓶子里的信息:执行任务的自行车拖车

> 原文：<https://hackaday.com/2020/06/19/message-in-a-bottle-bicycle-trailer-on-a-mission/>

涂鸦是一个有争议的话题，你是否将它视为艺术或破坏行为通常取决于你在哪里以及如何遇到它。从墙上潦草的标签，到高度复杂的壁画，它们往往有一个共同点:发表声明——无论是政治性的，表示赞赏，还是简单的“我在这里”。[Sagarrabanana]有他自己的说法，但选择了一种不太持久的方式来表达自己的涂鸦类型。

由于对自己所在地区缺乏专用自行车道感到不满，他建造了一辆由 Arduino 控制的自动喷水自行车拖车，在他骑行的每条街道上都写下了他的信息。视频中记录了建造过程[，另一个视频](https://www.youtube.com/watch?v=8DoLGqrMMEo)中显示了[的行动——这两个视频都是西班牙语的(也在休息后嵌入)，但图片在任何语言中都胜过千言万语。](https://www.youtube.com/watch?v=UZ8ayX4JWdI)

受[视觉暂留](https://hackaday.com/2019/10/29/the-basics-of-persistence-of-vision-projects/) (POV)的启发，移动的 led 同步闪烁以产生静态图像的幻觉，【Sagarrabanana】使用连接到水箱的螺线管阵列将概念转换为道路上的水。每个螺线管都由一个继电器控制，一个预定义的字体决定何时切换每个继电器——这与显示器上的像素被设置为开或关的方式相同，只是当自行车前进时会有少量的水喷出。消息本身通过串行蓝牙模块接收，并且可以很容易地修改，例如从电话。为了根据骑行速度调节水的分配，整个系统与安装在拖车车轮上的磁性开关同步，所以理论上你也可以带着它跑步。

时间会证明[Sagarrabanana]的任务是否会取得他所希望的成功，但毫无疑问，无论他去哪里，预告片都会吸引人们的注意。好吧，我们祝他一切顺利，不需要太激烈的替代写作媒介就能把信息传递出去。虽然，我们在过去已经见过使用粉笔喷雾的涂鸦机器人，所以如果需要的话，当然有空间进行不太永久的升级。

 [https://www.youtube.com/embed/8DoLGqrMMEo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8DoLGqrMMEo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent) 
 [https://www.youtube.com/embed/UZ8ayX4JWdI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UZ8ayX4JWdI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

