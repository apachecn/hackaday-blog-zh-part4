# 5 月 4 日，在你的手掌中享受一个 ASCII 版本的星球大战

> 原文：<https://hackaday.com/2021/05/04/enjoy-an-ascii-version-of-star-wars-in-the-palm-of-your-hand-for-may-the-4th/>

到目前为止，每个人可能都看过原版——也是最好的；《与我们战斗》——《星球大战》系列的一部分，很可能是它的 ASCII 艺术动画版本，通过消除所有令人分心的特效、人类演员和配乐，它在电影上有了很大的改进。但是到现在为止我们还没有的是[一个 ASCIIWars](https://gotohellmann.com/2021/04/29/asciiwars-on-youtube/) 的便携式播放器，让你在旅途中也能享受这部电影所有基于角色的荣耀。

虽然这种对[【西蒙·詹森】惊人的 ASCII 艺术成就](http://www.asciimation.co.nz/index.php)的致敬可能看起来像是对原作的简单重新包装，但【弗兰克】实际上不得不为完成这部作品付出一些努力。在得到[西蒙]的同意后，开始使用 WEMOS D1 Mini，这是一个很好的项目平台，无线功能更少，4 MB 闪存更多。选择 240×360 的 TFT LCD 显示器来放映影片；显示器的尺寸使得大多数字体难以阅读，所以[Frank]使用了[微微像素](https://blogfonts.com/picopixel.font)，这是一种为小屏幕上的易读性而设计的字体。动画文件存储在 D1 闪存上的 SPIFFS 文件系统中，几行代码解析它并将其发送到显示器。最后一点是安装一个旧的幻灯片浏览器，它可以放大显示屏，使其更容易看到。

尽管我们赞扬[弗兰克]对[西蒙]的努力的赞扬，但没有理由将这局限于《星球大战》的宇宙中。如果你熟读了[的 ASCII 艺术史](https://hackaday.com/2013/08/20/retrotechtacular-the-history-of-ansi-and-ascii-art/)，其中[追溯到惊人的久远](https://hackaday.com/2016/06/28/retrotechtacular-ascii-art-in-the-19th-century/)，你可能会受到启发，用 ASCII 码再现另一部经典电影，并放在这样的浏览器上。ASCII- *Metropolis* ，有人吗？

 [https://www.youtube.com/embed/Gn7KlUrOuFw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Gn7KlUrOuFw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

