# 在一百年前的打字机上敲出节拍

> 原文：<https://hackaday.com/2020/05/07/drumming-a-beat-on-a-hundred-year-old-typewriter/>

我们已经看到相当一部分不寻常的物品被变成了乐器。幸运的是，只要稍加修改，几乎任何东西都可以变成 MIDI 控制器。[William Sun Petrus]刚刚将一台 20 世纪 20 年代的打字机改造成了一台架子鼓，并在上面进行了一场精彩的现场表演。

构建相当简单，所有的(威廉·孙·彼特鲁斯)需要的是一个 Arduino Mega 和许多电线来将一台百年历史的雷明顿打字机转换成 MIDI 控制器。每当按下一个键时，锤子就会撞击打字机中心的金属板，并像普通按钮一样关闭 Arduino 的一个 IO 引脚和 5 V 轨之间的触点。Arduino 代码是基于 MIDI 库向运行 T2 无毛 MIDI 和 Ableton 的电脑发送命令。作为一种噱头，[威廉·孙·彼得鲁斯]包括一个液晶显示屏，每次按下一个键，就会显示苏斯博士的《T4 绿鸡蛋和火腿》中的一行。

有趣的是，由于锤子的旅行时间造成的延迟并不干扰[威廉·孙·彼得鲁斯的]现场播放。为了平息评论中的质疑，他还发布了一段未经编辑的视频[以证明表演是真实的，以及一段关于如何一个音符一个音符地演奏他的节拍的](https://youtu.be/QfHYKgnJjvs)[教学视频](https://youtu.be/RiQfWDHyFoU)。

其他不寻常的 MIDI 控制器包括 [bandoneon 手风琴](https://hackaday.com/2020/04/13/quieting-down-a-bandoneon-accordion-with-midi/)或[这种英国手风琴](https://hackaday.com/2019/08/18/midi-controller-in-a-concertina-looks-sea-shanty-ready/)。

休息后的视频。

 [https://www.youtube.com/embed/zbZ-oUly3QQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zbZ-oUly3QQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[感谢马库斯的提示]