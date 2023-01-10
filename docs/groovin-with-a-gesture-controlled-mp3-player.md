# 用手势控制的 MP3 播放器唱歌

> 原文：<https://hackaday.com/2021/11/06/groovin-with-a-gesture-controlled-mp3-player/>

触摸屏很棒，但它们并不总是完美的解决方案。试图戴着手套操作(即使是所谓的“触摸屏友好型”)可能会很麻烦，如果屏幕是在公共共享的设备上，如收银台，它很容易成为细菌，病毒和各种其他讨厌的东西的家。

这就是[诺伯特·扎雷亚]在制造他的手势控制 MP3 播放器时所想的。它使用 PAJ7620U2 手势传感器来记录一些直观的手部动作，包括手指转动来控制音量，手滑动来向前和向后跳过，以及一只平手来播放和暂停歌曲。它甚至有一个电动旋钮和可爱的剪切音符，可以移动以提供一些手势的视觉反馈，你可以在下面的视频中看到这一点。如果这看起来很熟悉，那是因为周二我们看了看他制作的基于摄像头的[扫视跳过轨迹控制器](https://hackaday.com/2021/11/02/computer-vision-lets-you-skip-songs-with-a-glance/)。

为了真正播放一些音乐，他拆除了一个旧 MP3 播放器的内部，并将控制按钮的焊盘连接到 Arduino，Arduino 从传感器读取手势信息，并通过将适当的引脚设置为高和低来模拟 MP3 播放器的按钮。最后，他用一个液晶显示屏和一个盒子结束了整个事情。

[诺伯特]方法的伟大之处在于它不仅仅局限于 MP3 播放器——它可以扩展到几乎任何设备上的按钮。因为 Arduino 只需要连接到设备的按钮输入，所以将大多数现有的触觉接口改造成免触摸应该相对容易。搭配我们今年早些时候看到的这个[手势跟踪宏键盘，](https://hackaday.com/2021/06/13/gesture-detecting-macro-keyboard-knows-what-you-want/)实际触摸我们的技术的日子可能很快就会成为过去。

 [https://www.youtube.com/embed/1hCQcGXv3D4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1hCQcGXv3D4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

