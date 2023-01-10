# 将旋转刀具转变为 CNC

> 原文：<https://hackaday.com/2018/11/16/turning-a-rotary-tool-into-a-cnc/>

现在 3D 打印机无处不在，电子产品很便宜，开源软件非常强大，几乎任何人都可以制造数控机床。这正是[Nikodem]所做的，他将 Dremel 工具[变成了一台极其强大的 CNC 机器](https://www.youtube.com/watch?v=239aFAqYBpQ)，能够切割 MDF 和丙烯酸树脂，还可以雕刻铝。

建造的电子设备只是一个 Arduino Uno，一个运行 [GRBL](https://github.com/gnea/grbl) 的电机驱动器 sheld，一个 Dremel 的继电器，几个电机驱动器和一个大的 30 安电源。构建使用 NEMA 17 电机，两个在 Y 轴上，一个在 X 轴和 z 轴上。尽管有 3D 打印零件，但 CNC 有一个非常坚固的框架。它由铝挤压而成，车厢骑在一些漂亮的直杆上。

至于这台数控机床工作的有多好，还是蛮不错的。使用 Gcode 从 MDF 中切割出直径为 80 毫米的圆，这台机器成功切割出直径为 80.02 毫米的圆。这是非常好的，并进入该领域的错误可能是在廉价的卡钳，而不是成品本身。这是一个令人敬畏的构建，[Nikodem]在他的四部分视频系列中记录了一切。你可以看看下面的结尾。

 [https://www.youtube.com/embed/239aFAqYBpQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/239aFAqYBpQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

