# 条形码吉他演奏的不仅仅是 Beep-Bop

> 原文：<https://hackaday.com/2019/09/26/barcode-guitar-plays-more-than-beep-bop/>

关于业余开发生态系统(如 Arduino)的兴起，我们最喜欢的一点是，现在几乎可以用任何东西来制作 MIDI 控制器，只要你有盾牌和奉献精神。我们很高兴[詹姆斯·布鲁顿]偶尔从制造机器人中抽身出来，转而从事仪器制造，因为他的最新发明使这一数字达到了 11。

这款出色的吉他使用条形码扫描仪来弹奏音符，并使用各种街机控件来操纵这些音符。条形码本身作为 ASCII 值扫描，它们的等效整数被发送到外部 MIDI 设备。这个未来主义的斧头是在 Arduino Mega 上建造的，有一个用于条形码扫描仪的 USB 盾，顶部有一个 MIDI 盾，休息后[James]可以连接到视频中的各种合成器。

在拍摄条形码的间隙，右手还用操纵杆控制八度音阶移动和改变 MIDI 通道，并用旋转编码器弯音。底部颈部的街机按钮阵列让他可以在单声道合成器的单人游戏和多人游戏之间切换。其他三个按钮是按下并扫描的可编程单音符发声器，有助于和弦制作和拨弄。

我们特别喜欢这种结构，它是 20/20 和 3D 打印盒子的结合。[James]找到了一些有角度的 PVC 作为四个琴颈的指板，还有一个不错的条形码背景。我们唯一要改变的是条形码扫描仪固有的蜂鸣声——要么让它永远静音，要么让它变得可变，因为它不会随着每个音符而摇摆。让枪连续扫描可能会很好，这样[詹姆斯]就不会有扣扳机的手指。或者更好的是，把扫描仪做成手套。

想用零件箱中的条形码扫描仪做些更有用的事情吗？[用它来管理你的家庭库存](https://hackaday.com/2018/04/23/bargain-bin-barcode-scanner-keeps-track-of-shopping-needs/)。但是首先，让你自己重新认识一下[由【亚当·法比奥】介绍的简陋条形码](https://hackaday.com/2015/11/02/the-eloquence-of-the-barcode/)的历史。

 [https://www.youtube.com/embed/OctazO-VxBw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OctazO-VxBw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢提示，[baldpower]！