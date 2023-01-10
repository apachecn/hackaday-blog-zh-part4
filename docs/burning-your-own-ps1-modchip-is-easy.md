# 烧你自己的 PS1 Modchip 很容易

> 原文：<https://hackaday.com/2020/11/01/burning-your-own-ps1-modchip-is-easy/>

最初的索尼 PlayStation 正好赶上了 CD 盗版真正开始流行的时候。意识到这种对销售的威胁，索尼的工程师们包括了一个拷贝保护和区域锁定机制，这既安抚了高管，也惹恼了终端用户。[MattKC]探讨了这种版权保护是如何工作的，[以及如何在家里只花几美元就能刻录自己的 modchip。](https://www.youtube.com/watch?v=INxyKrcYNoE)

索尼的版权保护方法依赖于制造过程中采取的步骤，在游戏媒体上压制一个普通 CD 刻录机无法复制的特殊凹槽，[我们自己的[Drew Littrell]已经深入探讨了这个主题](https://hackaday.com/2018/11/05/how-the-sony-playstation-was-hacked/)。这个凹槽包含一个四个字母的代码，可以被游戏机读取，对应于游戏销售的地区。控制台会在启动时读取这个凹槽，并在启动前检查游戏中的代码是否与控制台中的代码匹配。Modchips 通过在控制台中注入一个与本地区域匹配的欺骗代码来规避这一点，而不管从光盘上读取了什么。这使得用户既可以运行盗版 CD-r、自制代码，也可以运行其他地区的游戏。

今天，我们有幸拥有互联网和廉价的硬件。正如[MattKC]所展示的，现在已经没有必要从游戏杂志背面的虚假广告中邮购芯片了；相反，[人们可以下载源代码](https://quade.co/ps1-modchip-guide/mm3/)并将其闪存到一个商品 PIC 微控制器中，只需几美元。随着芯片焊接到 PS1 主板的相关点，你就可以走了。

就主机改装而言，PS1 是一个很好的平台——操作简单，也是有史以来最畅销的主机，所以如果你搞砸了，风险也很低。休息后的视频。

 [https://www.youtube.com/embed/INxyKrcYNoE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/INxyKrcYNoE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

