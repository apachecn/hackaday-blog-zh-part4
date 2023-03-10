# 带 1 马力隆隆声反馈的游戏

> 原文：<https://hackaday.com/2021/04/14/gaming-with-1-horsepower-of-rumble-feedback/>

力反馈在 90 年代末大规模兴起，给飞行操纵杆和赛车轮子带来了前所未有的真实感。它更便宜的触觉表亲是通过振动电机的隆隆声反馈，这确实增加了一些东西，但它更多的是一种感觉的想法，而不是与现实生活相关的任何东西。它通常也很弱，[但是【teenenggr】有办法解决这个问题。](https://teenenggr.com/2021/02/25/controller-rumble-is-not-enough-to-feel-the-game-just-rumble-everything/)

该版本采用常规的 Playstation 控制器，并断开内部隆隆电机。相反，控制器的电机输出与 Arduino Uno 的数字输入相连。当 Arduino 检测到隆隆声电机信号打开时，它会打开一个继电器，向一个大马力的感应电机供电，电机上装有一个偏心重量。

接下来发生的是纯粹的混乱。本质上相当于把砖头扔进洗衣机，只要有一点点来自增益的隆隆声信号，马达就会震动整个桌子。持续震动命令，比如在*孤岛危机里开机枪的时候，*把【teenenggr】的显示器从桌子上摔下来。即使用胶带粘好了，玩游戏也很快变得不可能，因为他无意中按下了 ALT-Tab 并离开了游戏，同时试图抓住桌子不放。

是有用的黑客吗？不，但如果它被栓在你朋友的游戏装备下，会成为一个很好的恶作剧。也就是说，强烈的振动可能不会对机械硬盘驱动器、任何带有 edge 连接器的设备或只是他们的电脑有任何好处。这是我们上一个[teenenggr]项目的一大进步——[一个隆隆声反馈鼠标。](https://hackaday.com/2020/05/17/force-feedback-mouse-really-shakes-things-up/)休息后的视频。


 [https://www.youtube.com/embed/fxmLD8y0RNQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fxmLD8y0RNQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

