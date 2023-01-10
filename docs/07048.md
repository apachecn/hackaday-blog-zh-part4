# N64 上的远程代码执行

> 原文：<https://hackaday.com/2020/07/06/remote-code-execution-on-the-n64/>

一些人喜欢在业余时间园艺，而另一些人喜欢抽雪茄或折叠复杂的折纸小雕像。安全研究员~~【骗子】~~【CTurt】似乎更喜欢破解控制台，并尝试过[通过一个模糊的调制解调器接口](https://cturt.github.io/shogihax.html)开发任天堂 64。

20 世纪 90 年代是一个疯狂的时代，游戏都是盒装的。这种格式为盒式磁带本身增加额外的硬件提供了极大的可能性。也许最著名的是，任天堂在 SuperFX 芯片中加入了 3D 图形功能。后来，N64 游戏 Morita Shogi 64 自带了一个完整的电话调制解调器。由此产生的漏洞因此被称为“shogihax”。

装备了一个狡猾的游戏沙克和一个反编译器，[CTurt]开始工作。通过仔细解析代码，他们能够在使用调制解调器时找到游戏中合适的溢出漏洞。与更普通的 savegame hacks 不同，这不仅允许执行任意代码，而且调制解调器接口意味着有可能在特定的基础上不断向控制台传输更多的数据。

这是一个很好的黑客技术，它利用了相对容易获得的盒式磁带，而不是依赖于更模糊的硬件，如 N64DD 调制解调器或其他稀有设备。[我们以前也见过其他的 N64 自制黑客](https://hackaday.com/2019/01/11/nintendo-64-homebrew-via-game-shark/)。休息后的视频。

感谢[骗子]的提示！

 [https://www.youtube.com/embed/9VyoLYnWx7o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9VyoLYnWx7o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

