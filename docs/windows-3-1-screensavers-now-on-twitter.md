# Windows 3.1 屏保，现在在 Twitter 上

> 原文：<https://hackaday.com/2019/09/23/windows-3-1-screensavers-now-on-twitter/>

回到 GUI 时代的早期，阴极射线管是个人电脑的主要显示技术。为了避免静态显示元素的老化，设计了屏保来帮助防止这个问题。出于对昔日软件的热爱，格雷格·肯尼迪(Greg Kennedy)设计了一个机器人，在 Twitter 上发布 Windows 3.1 屏保。

在这种情况下，Perl 脚本运行该显示。屏保被打包成“单元”，由脚本加载。然后配置一个基本的 Windows 3.1 环境，并将其加载到一个专门打了补丁的 DOSBOX 中，该 DOSBOX 允许在一个无头环境中自动录制演示。一旦启动并运行，视频记录在桌面上，随后触发屏幕保护程序。几分钟后，录制停止，FFMPEG 用于将视频转码为适合 Twitter 的格式。然后，使用标准 API 发布视频就很简单了。

这是一个有趣的项目，使共享旧的屏幕保护程序变得容易。请务必查看 Twitter feed @dot_scr。如果你沉迷于复古美学，[在你的 Linux boxen 上试试这个苹果【屏保破解】。](https://hackaday.com/2014/07/18/apple-graphics-as-your-screensaver-or-second-screen/)休息后的视频。

> 名称:土星
> 作者:微软/ HyperDyne 2000 软件
> 设置:(无)【pic.twitter.com/6C7mXGtheY】T2
> 
> — Windows 3.1 屏保(@ dot _ SCR)[2019 年 9 月 21 日](https://twitter.com/dot_scr/status/1175313169327230982?ref_src=twsrc%5Etfw)