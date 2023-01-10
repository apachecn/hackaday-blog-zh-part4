# 少摇滚，多摇滚:一架 MIDI 桶形钢琴

> 原文：<https://hackaday.com/2020/06/18/less-rock-more-roll-a-midi-barrel-piano/>

在任何大城市的公园、步行区或旅游区漫步，很少能不听到管风琴的声音——如果你的音乐技能是手臂耐力和稳定的旋转速度，这是一种完美的乐器。它不太常见的表亲，也是自动演奏钢琴的前身，是桶式钢琴，它遵循相同的演奏原理:手动曲柄转动桶，桶上的销钉或穿孔纸卷对它应该拨动的琴弦进行编码，以便演奏其编程的歌曲。[gabbapeople]认为光耦合器将是这里的完美选择，[并与他们一起建造了一架 MIDI 桶形钢琴](https://www.instructables.com/id/Arduino-Barrel-Piano/)。

保持经典的手动手摇曲柄，3D 打印的齿轮机构在树脂玻璃固定装置上滚动纸张，但[gabbapeople]的钢琴不是在上面打孔，而是在上面打印简单的标记。这些标记由一组连接到 Arduino 的 [*Octoliner*](https://my.amperka.com/modules/octoliner) 模块读取。Octoliner 本身有八对红外发光二极管和光电晶体管排成一行，通常用于制造循线机器人，因此阅读笔记标记肯定是它的一个聪明的替代用途。

每个 LED/晶体管对代表一个专用的音符，为了防止来自相邻线的假阳性，[gabbapeople] 3D 打印的小项圈隔离了每一对。一旦信号被 Arduino 读取，它们就被转换成 MIDI 信息，通过 USB 发送到运行任何类型软件合成器的电脑。如果你的手确实累了，你也可以用电钻转动它，正如休息后的视频所示，还有一些回放演示。

看到老派乐器加入现代元素总是很有趣，尤其是那些不是典型的 MIDI 控制器的乐器，比如[竖琴](https://hackaday.com/2019/08/17/midi-harp-looks-pretty-sharp/)，全尺寸[教堂风琴](https://hackaday.com/2020/04/09/controlling-a-building-sized-pipe-organ-with-midi/)，当然还有名副其实的[风琴](https://hackaday.com/2018/10/25/hurdy-gurdy-gets-modernized-with-midi-upgrades/)。关于[gabbapeople]的更多作品，请查看他的分屏天气显示。

 [https://www.youtube.com/embed/-rObmt3vAhc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-rObmt3vAhc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent) 
 [https://www.youtube.com/embed/pX_CWn_gZyo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pX_CWn_gZyo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

