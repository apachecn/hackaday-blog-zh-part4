# BlixTerm 为 Commodore 宠物带来了全速 YouTube 视频

> 原文：<https://hackaday.com/2022/07/01/blixterm-brings-full-speed-youtube-video-to-the-commodore-pet/>

如果你曾经使用过 20 世纪 70 年代末或 80 年代初的家用电脑，你肯定会对它们缓慢的用户界面很熟悉。甚至从 ram 中列出一个 BASIC 程序的内容也需要几秒钟，屏幕一次更新一行。视频游戏完全针对速度进行了优化，但仍然可以同时处理几个缓慢移动的物体。显然，在那个时代的硬件上播放类似全动态视频的东西是绝对不可能的——或者你可能会这么想。

事实上，[thorbjrn je mander]已经成功说服一只准将宠物以完全合理的每秒 30 帧的速度播放 YouTube 视频。他在视频中描述了设计“BlixTerm”硬件和软件的过程(嵌入在下面)，以及许多关于如何将数字系统推向绝对极限的有用信息。

[![A video of a drifting car, as rendered by a Commodore PET display](img/33cdb2c4f99aeceb5bff62331b8e4896.png)](https://hackaday.com/wp-content/uploads/2022/06/Commodore-PET-Youtube-video.gif) 自然，宠物需要现代硬件的一点帮助，在这种情况下，一个树莓派零 2 W 连接到“用户”扩展端口。Pi 通过 WiFi 连接到 YouTube 并加载所请求的视频，然后将其向下转换为 640×200 灰度流，并将每一帧转换为 80×25 字符网格，使用宠物 rom 中最接近所需模式的字符。

虽然要从 Pi 中挤出足够的性能来实时完成所有这些需要相当大的努力，但最棘手的是如何将结果字符流足够快地放入宠物的视频内存中。为了做到这一点，[thorbjrn]设计了一个具有 2 KB 双端口 SRAM 的特殊接口卡，使 Pi 能够在一端准备好视频帧后立即存储它们，而宠物则可以按照自己的速度从另一端加载它们。由于只有 16 微秒的时间来处理每个字节，宠物的 CPU 只能执行 4 到 5 条机器代码指令；仅够加载和存储一个字符并跳转到下一个内存地址。

最后的结果，正如你在视频中看到的，真的令人印象深刻。即使在 Commodore 字符集的限制下，生成的图像也清晰可辨，而帧速率似乎不受硬件的限制。

如果你是一个 Commodore 迷，想知道那个奇怪的 PET 600 模型到底是怎么回事，[thorbjrn][也制作了一个关于它的视频](https://www.youtube.com/watch?v=FkZtM4YTRiQ)；这是针对瑞典市场的改款 8296。我们之前实际上已经看到过[在宠物](https://hackaday.com/2014/04/06/vcf-east-petpix-streaming-images-to-a-commodore-pet/)上生成实时视频的项目，尽管帧率要低得多。感谢提示，[基思奥尔森]！

 [https://www.youtube.com/embed/4e0fRKHG7Hk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4e0fRKHG7Hk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

