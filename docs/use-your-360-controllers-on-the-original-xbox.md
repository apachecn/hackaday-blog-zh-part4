# 在原始 Xbox 上使用您的 360 控制器

> 原文：<https://hackaday.com/2019/02/08/use-your-360-controllers-on-the-original-xbox/>

微软最初的 Xbox 在发布时受到了游戏玩家和媒体的好奇关注。它更大，更笨重，以一个怪异的怪物作为它的原始控制器。令人欣慰的是，微软认为应该在游戏机寿命的后期用控制器 S 来改进一些东西，但没有什么能与 Xbox 360 控制器的简单荣耀相比。现在，有一种方法可以在你原来的 Xbox 上使用。

这个项目是[Ryzee119]，[的作品，他之前改编了控制器用于任天堂 64。](https://hackaday.com/2018/07/31/add-on-board-brings-xbox-360-controllers-to-n64/)充当主控制器的 Arduino Pro Micro 与 MAX3421 USB 主控制器对话，后者与 Xbox 360 无线接收器(正版或第三方)接口。Arduino 从无线接收器读取数据，然后模拟原始 Xbox 的标准控制器。该系统可以在 wireless 360 控制器上处理多达四个播放器，每个控制器需要一个额外的 Arduino，以从模式运行，并将信号模拟到原始 Xbox。在测试中，[滞后似乎与原始有线控制器](https://www.youtube.com/watch?v=V7Pnba7Y12Y&feature=youtu.be)大致相当。对于快节奏的动作游戏或任何基于节奏的游戏来说，这是一个特别重要的考虑因素。

这是一个执行良好，功能齐全的项目，应该可以极大地改善你的每周光晕 2 局域网党。格雷格再也不会被控制器电缆绊倒，把多力多滋和激浪洒在你的毛绒地毯上了。休息后的视频。

【感谢 DJ Biohazard 的提示！]

 [https://www.youtube.com/embed/ycZjQUjz1Fk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ycZjQUjz1Fk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/V7Pnba7Y12Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/V7Pnba7Y12Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

