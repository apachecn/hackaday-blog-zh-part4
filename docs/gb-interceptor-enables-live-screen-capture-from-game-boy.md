# GB 拦截器支持 Game Boy 的实时屏幕捕捉

> 原文：<https://hackaday.com/2022/12/22/gb-interceptor-enables-live-screen-capture-from-game-boy/>

[塞巴斯蒂安]有一个棘手的问题要解决。俄罗斯方块锦标赛的参赛者需要流式传输他们的 Game Boy 屏幕视频，但没有现成的解决方案。出于公平的原因，模拟器是正确的，也不能修改游戏男孩。因此，【塞巴斯蒂安】创造了[GB 拦截器，一个游戏男孩捕捉盒](https://www.youtube.com/watch?v=6mOJtrFnawk)。

由于 Game Boy 的设计，通过盒式磁带端口本身可以获得大量有用的信号。[Sebastian]意识到可以制造一种非侵入性的捕捉设备，放在游戏机和手推车之间，将视频发送到计算机。不幸的是，不能通过这个端口直接访问显存，但是[Sebastian]找到了一个巧妙的解决方法。

构建使用了一个树莓派微微。该芯片的两个内核分别模拟 Game Boy 的 CPU 和图片处理单元。要做到这一点，同时让芯片跟上 Game Boy 的发展，需要将 Pico 超频到 225 MHz。该系统的工作原理是从卡带的内存总线上获取数据，并遵循游戏机运行的指令。通过这样做，Pico 能够填充它自己的视频 RAM 副本。然后，它通过 USB 接口将这些内容发送出去，并根据需要在网上显示和传输。

虽然存在一些极限情况的限制，但就其预期目的而言，该系统运行良好。目前，该硬件可以在 Linux 和 Windows 上使用，尽管在后一种情况下它需要一些改动。Github 上的文件是为那些渴望建立自己的文件的人准备的。如果你只是想扔掉购物车，而不是从你的游戏机上下载，我们也可以提供帮助。休息后的视频。

 [https://www.youtube.com/embed/6mOJtrFnawk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6mOJtrFnawk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

