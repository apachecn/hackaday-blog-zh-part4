# 通过连接线端口转储 Game Boy 墨盒

> 原文：<https://hackaday.com/2022/12/14/dumping-game-boy-cartridges-via-the-link-cable-port/>

当谈到像 Game Boy 这样的老式游戏机时，能够为后代、存档和仿真转储盒式 rom 通常是很好的。为此，[Low Byte Productions]的[[Francis Stokes]想出了一个相当独特的方法，通过链接电缆端口转储游戏机推车。](https://www.youtube.com/watch?v=rORPp6vYMsw)

该方法首先在由 flash cart 交付的 Game Boy 上运行定制代码。该代码将自身加载到 RAM 中，然后等待用户换入他们希望卸载的购物车并按下按钮。然后，代码一个字节一个字节地读取盒式磁带，并通过链接端口将其发送出去。为了获取数据，[Francis]只需使用 Saleae 逻辑分析仪来完成这项工作。值得注意的是，这种方法最初的错误率非常高，直到[Francis]意识到缩短链接电缆的长度可以减少干扰信号的噪声。

感兴趣的人可以在 GitHub 上找到代码[。](https://github.com/francisrstokes/tega/tree/main/src/rom-dumper)[当然还有其他方法可以扔掉 Game Boy 墨盒](https://hackaday.com/2011/03/20/gameboy-rom-backups-using-an-arduino/)。

 [https://www.youtube.com/embed/rORPp6vYMsw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rORPp6vYMsw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

