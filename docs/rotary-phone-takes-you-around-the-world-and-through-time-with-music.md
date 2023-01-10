# 旋转电话带你环游世界，穿越时间——伴着音乐

> 原文：<https://hackaday.com/2020/06/24/rotary-phone-takes-you-around-the-world-and-through-time-with-music/>

有目的地选择过时的技术将简单时代的所有快乐与知道自己实际上没有被过时的(通常是低劣的)技术束缚的舒适结合在一起。旋转式电话是一个很好的例子，虽然很少有人愿意回到每天用它拨打电话的冗长、容易出错的方式，但它绝对可以为一个项目增添某种魅力。卡罗琳·巴特也是这么想的，她把她奶奶的旧旋转电话变成了一个可以穿越时间、环游世界的网络收音机。

主要的想法相当简单:一个树莓派通过浏览器连接到一个网络电台网站，播放几十年来来自世界各地的音乐。[Caroline]的实现有一些不错的变化。首先，当然是手机，它不仅有 Raspberry Pi，还可以通过手机扬声器作为实际的收听设备，并作为输入设备通过旋转拨号选择十年。对于一个无头设置，她编写了一个 Chromium 扩展，将按键事件映射到网站相应 DOM 元素上的虚拟点击——就像那些改变十年的按钮——以及一个 Python 脚本，将旋转拨号脉冲转化为这些按键事件。

然而，手机只是故事的一半，国家的选择也同样令人着迷——这涉及到实际的世界地图。每个可选国家都配有一个音频连接器，并连接到 Arduino。如果匹配的插孔插入其中，Arduino 会通过串行线通知 Raspberry Pi 新的选择，然后相同的 Chromium 扩展会触发底层网站的国家更改。你可以在[项目的 GitHub 库](https://github.com/carolinebuttet/rotary-radio)中检查所有代码，休息后观看视频中的演示和简要说明。

当然，通过电话收听广播可能不是最方便的方式——除非它是合适的类型——但这显然不是这里的目标。这绝对是一个有趣的概念，我们可以很容易地看到它转移到一些旅游或间谍主题的逃生室设置。说到间谍活动，如果[Caroline]的名字你听起来很熟悉，你可能记得几个月前[她的虚拟窥视孔](https://hackaday.com/2020/02/18/insecure-surveillance-cameras-provide-dystopian-peep-show/)。

 [https://www.youtube.com/embed/Wz1SBkfLXiY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Wz1SBkfLXiY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent) 
 [https://www.youtube.com/embed/5mjZgalAXfs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5mjZgalAXfs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

