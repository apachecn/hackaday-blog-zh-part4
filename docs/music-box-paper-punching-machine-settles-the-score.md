# 八音盒打孔机结算分数

> 原文：<https://hackaday.com/2019/11/15/music-box-paper-punching-machine-settles-the-score/>

当(pashiran)第一眼看到他的第一个手摇音乐盒时，他就知道他恋爱了。然后，他开始为他的第一首小曲打洞。随着重复的击打压力使他的手臂发热，他的爱冷却了一些。这次经历的起伏磨练了他，他决定设计一台能自动打孔的机器。

很快，[pashiran]找到了他的人——[一个音乐拳击手社区](https://musicboxmaniacs.com)，他们将 MIDI 文件转换成 DXF 格式，为 CAD 软件创建坐标。在[pashiran]的音乐穿孔机中，一个 Arduino MEGA 拿着一个 DXF 文件，对一堆杂乱的 x 坐标进行冒泡排序。MEGA 由两台步进电机和 DC 电机组成。一个步进器在 x 轴上推动纸张，另一个步进器在 y 轴上来回移动打孔机头。DC 马达上下移动打孔机。

现在，与[Wintergatan]的[将音乐盒纸连接在一起的方法](https://www.youtube.com/watch?v=HjBhO9iqEc0)结合起来，[pashiran]可以写出一部摇滚长度的作品，而不用担心重复的压力伤害。既然他已经出版了 STL 和 INO 文件，现在你也可以了。休息之后，观看它打卡并播放价值 250 个音符的“~~”~~“请便”。

避免手动打孔的方法不止一种。当[Wintergatan]在解决这个问题时，[他启发黑客社区创造了一个 MIDI 到激光切割模板的解决方案](https://hackaday.com/2017/05/06/ad-hoc-midi-to-music-box-project-shows-power-of-hacker-community/)。

 [https://www.youtube.com/embed/Lov9hmhkNws?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Lov9hmhkNws?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

