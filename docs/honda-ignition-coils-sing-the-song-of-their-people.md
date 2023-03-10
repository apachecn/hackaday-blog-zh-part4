# 本田点火线圈唱他们的人民之歌

> 原文：<https://hackaday.com/2022/01/11/honda-ignition-coils-sing-the-song-of-their-people/>

几十年来，高压实验人员一直在家庭实验室中使用汽车点火线圈来产生令人印象深刻的火花，为什么不呢？它们很便宜，很容易获得，而且在一天结束时，产生火花正是它们的设计目的。但这并不意味着没有改进的余地。

[在他最新的*等离子频道*视频中【Jay Bowles】重温了这个经典实验](https://www.youtube.com/watch?v=YVHIKee-fhE)，带来了他在过去几年中获得的大量高压经验。基于早期使用单个本田点火线圈的设置，这种新的双线圈版本可以产生高达 60，000 伏的电压，并由基于标志性的 555 定时器的更清洁、更可靠的电路驱动。驱动器前面的一对电位计可以手动调整其方波输出，范围为 1 至 10 千赫，而连接到 555 电路的商用蓝牙音频接收器只需播放配对设备的音频即可调制输出。

[![](img/0bd33ea9e38a81485648f205a22bcce9.png)](https://hackaday.com/wp-content/uploads/2022/01/dualcoils_detail.jpg) 正如【杰伊】所解释的，给一个基本的点火线圈接线非常简单。通常只有三个端子:正负输入和一个高压输出。但在这种情况下，由于他驱动两个线圈，他实际上是反向连线。用螺栓固定在一个漂亮的丙烯酸支架上，用香蕉插头提供大约 18-25 伏的直流输入，你就有了一个紧凑可靠的高压电源。驱动器本身是他在过去的项目中使用的电路的[进化版本，除了增加蓝牙音频输入，现在还具有一个缓冲电路，以帮助防止 555 被煮熟。](https://hackaday.com/2019/09/14/subaru-coils-make-a-great-hv-power-source/)

那么结果如何呢？首先，有很多美丽的火花。但是通过蓝牙播放音频，双线圈之间的电弧将充当等离子扬声器。输出是清晰的，但不是非常响亮。根据[Jay]的说法，这是因为点火线圈不应该在如此高的频率下驱动，结果会降低输出电压。但正如视频结尾所展示的那样，事实证明，从这个装置中获取音频的方法不止一种；随着天线连接到线圈的输出，该系统成为一个无线电发射机。

在市场上寻找更多的高电压乐趣使用 555？[看看这个由](https://hackaday.com/2019/12/09/drive-a-plasma-ball-with-an-atv-ignition-coil-and-a-555/)[驱动的 DIY 等离子球](https://hackaday.com/2018/10/10/the-555-and-how-it-got-that-way/)，这个五十岁的集成电路让硬件黑客们爱不释手。

 [https://www.youtube.com/embed/YVHIKee-fhE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YVHIKee-fhE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

