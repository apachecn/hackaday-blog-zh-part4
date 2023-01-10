# 自解魔方

> 原文：<https://hackaday.com/2018/09/24/self-solving-rubiks-cube/>

魔方似乎已经存在了很长时间，并且已经产生了一种致力于用自动化解决这个难题的亚文化。大多数魔方机器人将魔方放在一个特别设计的支架上，支架上布满了致动器和传感器，尽管这些装置令人印象深刻，但它们无法与魔方本身内置的机器人魔方解算器相提并论。

公平的警告，[人类控制者]除了图片没有提供更多的细节；即使翻译日文网页也不能提供更多的信息。但有图片，加上下面的视频，揭示了标准尺寸的魔方内包装的工程杰作。原始立方体的内部机制已被一个球形组件所取代，立方体的面围绕该球形组件旋转。这个看起来是 3D 打印的球体包含六个电机和齿轮系，以及一个微控制器板和一个看起来是霍尔传感器板的东西，用于检测每个面部的位置。所有东西都用电磁线连接起来，以保持捆绑的最小尺寸，深埋在里面的是一个脂肪电池组。一段拆卸视频为这个精巧装置的内部运作提供了进一步的线索。

一旦立方体感觉到它被打乱了，它就开始解决问题，在这个过程中，它在桌子上走来走去。很明显，它不只是记录加扰步骤，并反向播放它们；下面的视频显示，解决立方体的移动次数远远超过了 15 次。

虽然我们总是对速度的奇迹印象深刻，比如这个解决时间为 637 毫秒的[机器人，](https://hackaday.com/2018/03/12/rubiks-robot-so-fast-it-looks-like-a-glitch-in-the-matrix/)把解决立方体所需的一切都放在里面是一个值得庆祝的壮举。这里希望一个构建日志很快出现，以满足我们对细节的需求。

 [https://www.youtube.com/embed/xCoH2AORcEQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xCoH2AORcEQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/cExtbByvAEw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cExtbByvAEw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[jackw01]和[rasz_pl]的提醒。