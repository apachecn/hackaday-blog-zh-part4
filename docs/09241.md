# RFID 音乐播放器让整个房子都沸腾了

> 原文：<https://hackaday.com/2021/02/13/rfid-music-player-gets-the-whole-house-pumping/>

RFID 标签通常用于行人任务，如跟踪运输板条箱或打开我们宁愿不去的工作场所的门，但它们也可以很酷和有趣。[[hove Eman]用一个整洁的点唱机项目巧妙地证明了这一点。](https://github.com/hoveeman/music-cards)

这个建筑是基于一个藏在桌子下面的树莓派 Zero，上面有一个 USB RFID 阅读器。桌子上面是一系列的 RFID 卡，[hoveeman]用喷墨打印机中的特殊盒子在上面打印出他最喜欢的专辑的插图。通过一些 Python 代码和 shell 脚本，当扫描一张卡时，Pi Zero 能够触发家中所有的 Google Home 兼容设备同时播放所选的专辑。

这是一种视觉上令人愉快的提示音乐的方式，可能比大多数语音助手更可靠。我们可以看到这对威泽的粉丝特别有用；在该乐队的许多同名专辑中，Siri 和谷歌助手通常无法根据要求播放正确的专辑。我们以前见过其他漂亮的 RFID 自动点唱机，但是一个真正突出的玩家抛弃了射频，只使用计算机视觉和黑胶唱片作为 ID。

 [https://www.youtube.com/embed/AvCseOQidSw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AvCseOQidSw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

