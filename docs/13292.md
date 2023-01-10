# 使用这款面部键盘，通过抽动和眨眼来打字

> 原文：<https://hackaday.com/2022/04/09/twitch-and-blink-your-way-through-typing-with-this-facial-keyboard/>

对于那些没有经历过的人来说，至少可以说，为人父母的早期是具有挑战性的。试图在睡眠剥夺的情况下完成任何事情已经够难的了，但是这个似乎总是需要和你身体接触的小家伙让用手做事变得几乎不可能。当要找到有收入的工作时，初为人父母的人应该做些什么？

发现自己处于这样的困境，[Fletcher]的解决方案是制造[一个面部激活键盘](https://youtu.be/rZ0DBi1avMM)来满足他后代的需求。在你问之前:不，语音识别软件不会工作，至少根据那些抗议吵闹醒来的瞌睡小老板所说。相反，解决方案是首先尝试 OpenCV 和 dlib 面部识别库来观看[Fletcher]闪烁出莫尔斯电码。虽然这有点奏效，但一个人的眼睛无法长时间忍受这样的锻炼，所以他转向了一套更简单的手势。口型莫尔斯电码覆盖了键盘的大部分，而眼睛、眉毛和其他面部抽搐的组合覆盖了其余部分，MediaPipe 的面部网格在地标检测方面做了大量工作。

由此产生的面部键盘被恰当地称为[“CheekyKeys”，](https://github.com/everythingishacked/CheekyKeys)表现良好，足以让【弗莱彻】在一家大型科技公司的面试中用于技能测试。想象面试官在另一端看着他在面试中抽搐，这是值得的，我们甚至不在乎这是不是一个骗局。休息后的视频。

CheekyKeys 非常酷，用网络摄像头和 Python 做了一些我们认为需要专用人工智能深度摄像头才能完成的事情。但也许真正的诀窍是[弗莱彻]如何在 15 分钟内自学了莫尔斯。

 [https://www.youtube.com/embed/rZ0DBi1avMM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rZ0DBi1avMM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

