# 教老式行式打印机做音乐，从头再来

> 原文：<https://hackaday.com/2019/09/13/teaching-a-vintage-line-printer-to-make-music-all-over-again/>

坐在任何机器旁边足够长的时间，你就会通过它发出的声音来了解它。想想来自任何 3D 打印机或数控机器的声音；例如，不用看就很容易知道 g 代码何时通过正弦和余弦来画圆。

那时候也是一样，无聊而聪明的软件工程师听到他们的设备发出类似音符的声音，然后编写程序把它们变成粗糙的音乐机器。现在，[Ken Shirriff]详细介绍了他为恢复一台老式 IBM 1403 行式打印机的音乐功能所做的努力。这个巨大的 20 世纪 60 年代的野兽现在是一个不可替代的博物馆藏品，但当[Ken]和他在计算机历史博物馆的朋友们挖掘出一堆标有歌曲名称的穿孔卡片时，如“在风中飘荡”和“蓝色多瑙河华尔兹”，他们决定试一试。

1403 行式打印机有一个独特的链传动打印头，其内部工作原理[Ken]在他的文章中详细描述。给定固定且精确控制的旋转链速度，通过计算出需要哪些字符序列来获得特定频率来演奏音符。这种技术非常类似于乐器使用的技术，例如[电子琴](https://hackaday.com/2016/07/13/nirvana-like-youve-never-heard-them-before/)，或者当从[日常用品包括电动牙刷](https://hackaday.com/2019/08/23/when-toothbrushes-typewriters-and-credit-card-machines-form-a-band/)中强制播放音乐时。

由于缺乏音乐程序的源代码，[Ken]不得不对编译后的程序进行逆向工程，以了解其工作原理，并查看播放音乐是否会损坏链传动。下面的视频显示打印机安全地通过一个小[德彪西]；1970 年最初录制的歌曲的音频剪辑也可以获得。

 [https://www.youtube.com/embed/Lu4SxJqU9I4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Lu4SxJqU9I4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

