# 黑客驱动构建 R/C Forza 控制器

> 原文：<https://hackaday.com/2020/09/02/hacker-driven-to-build-r-c-forza-controller/>

自从 Atari 操纵杆的硬角出现以来，普通的视频游戏控制台控制器已经变得更好，更符合人体工程学。尽管游戏已经变得如此美丽和引人入胜，但控制器仍然是最不吸引人的方面。当你可以假装它们都是遥控汽车时，为什么要用一个普通的控制器来驾驶你可爱的车队呢？

[![](img/e1ea898374b1b6fbc10b2630c3f4b65c.png)](https://hackaday.com/wp-content/uploads/2020/08/forza-controller-receiver-guts.jpg) 【戴夫】在贝佐斯的仓库里找到了一款价格实惠的 4 通道遥控控制器，并照做了。它需要一些修改才能工作，比如制作一个子板，将拇指握持输入从切换按钮变为瞬时输入，并弄清楚如何处理三向滑动开关，但它看起来像是一个爆炸式的使用。

控制器有 6 通道版本，顶部有两个电位计。两个版本都有相同的外壳和 PCB，所以当[Dave]决定在那里安装一对瞬时按钮时，他已经为自己设计好了位置。这些基于三向滑块位置改变角色，在比赛模式、菜单模式和附加模式之间切换。

我们喜欢[Dave]将原始接收器变成模拟 Xbox 360 控制器的 USB 加密狗的方式——他用一个公 USB-A 自制了一个 Arduino Pro Micro，拆下接收器板，然后用电线将它们连接在一起。关于这一点有一个完整的单独的博客帖子，你制作自己的 R/C 控制器所需的一切都在 GitHub 上。休息后，请查看控件的演示和概述。

[Dave]对制作游戏控制器并不陌生——几个月前我们展示了他的[DJ Hero 控制器，该控制器经过修改可以玩旋转节奏 XD。](https://hackaday.com/2020/02/24/dj-hero-controller-gets-a-new-gig/)

 [https://www.youtube.com/embed/1TbkDqz1I3M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1TbkDqz1I3M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



通过 [r/duino](https://www.reddit.com/r/arduino/comments/iidrgw/i_turned_this_rc_remote_into_a_controller_for/)