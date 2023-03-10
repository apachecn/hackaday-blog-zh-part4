# PC 扬声器作为新专辑继续存在

> 原文：<https://hackaday.com/2019/02/23/the-pc-speaker-lives-on-as-a-new-album/>

最初的 IBM 个人电脑中的扬声器几乎是有史以来最差的电子乐器。这并不是因为令人惊叹的艺术作品从来不是为电脑扬声器创造的；不，已经有人做过了，而且很神奇。PC 音箱很可怕，因为它是多么有限。它在 8253 可编程间隔定时器的驱动下，一次只做一个音符，只有方波。复调？别提了。音量控制？没有。这些并不是真正的缺点，因为音乐是艺术，你可以不用字母“E”来写小说；诀窍在于你如何设法去做。

【shiru8bit】深究 PC 音箱[决定出专辑](https://habr.com/en/post/439192/)。视频，配有完全必要的 CRT 图形显示，[可以在这里看到](https://www.youtube.com/watch?v=tUy1MEpqbvk)。仅此一点就令人印象深刻，但这张专辑是如何发生的才令人惊叹。

如果你想在电脑扬声器上演奏不止一段简单的旋律，有两种或两种半的方法可以做到。第一种是(虚拟地)建立两个(或更多)通道，加载频率值。在设定的时间间隔，CPU 改变 8253 输出一个频率，然后在下一个时间段，将 8253 设置为另一个频率。由于缺乏更好的术语，这听起来有些“泡沫”，但结果可能是惊人的；只需查看一下*猴岛*T3 的 PC 音箱版本[。8253 也可以变成一个基本的 DAC，但由于专利，这是一项罕见的技术，到专利到期时，每个人都已经有了 Soundblaster。哦好吧。](https://www.youtube.com/watch?v=1IOL4q5tDDQ)

[shiru8bit]的专辑使用了第一种技术，在 120 Hz 的单声道方波中循环，但这里真正的技巧是单个通道是如何组成的。这需要创建一个名为 PCSPE 的 VSTi 插件。这模仿了一个电脑扬声器，并实现了不同声道的琶音、音高和优先级。实际上，这是一个电脑扬声器跟踪器。

结果是经典的 chip tune good，在一种真的不应该用于音乐的乐器上制作。它可以在 DosBox 上播放，但真实硬件的怪异之处(包括瞬变和微型扬声器的低效率)使得真实硬件在这里几乎是必要的。你可以看看下面的整张专辑。

 [https://www.youtube.com/embed/tUy1MEpqbvk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tUy1MEpqbvk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

