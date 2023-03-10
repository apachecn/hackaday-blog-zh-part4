# FPS 游戏的触觉反馈依赖于 OpenCV

> 原文：<https://hackaday.com/2021/03/31/haptic-feedback-for-fps-games-relies-on-opencv/>

个人电脑游戏玩家认为他们的平台在强大的处理能力和固有的可定制性方面更胜一筹。它们令人失望的地方可能是典型的键盘和鼠标界面，它倾向于避免一些花哨的功能，如触觉反馈，这些功能长期以来一直是游戏机的标准。为了纠正这一点，[【中微子-1】为 FPS 游戏组装了一个奇特的触觉反馈系统。](https://www.instructables.com/Gamer-Assist-a-Haptic-Feedback-System-for-Games-Us/)

黑客相当优雅，使用 Python 应用程序来抓取 FPS 游戏的 GUI 以获得健康读数。使用 OpenCV 进行光学字符识别来收集健康数据，并通过 USB 串行连接将结果数据发送到 ESP12E 微控制器。然后，ESP12E 控制一系列新像素 led 和振动电机，根据用户在游戏中的健康状况变化提供颜色和触觉反馈。

使用图像识别可以让系统快速重新配置，以适应不同的游戏，而不必为每个不同的游戏学习不同的 API。这是一种非常有趣的方式，可以快速地让一个项目与一个我们希望在未来看到更多的软件进行交互。它是对我们在这个领域看到的其他黑客攻击的一个很好的补充，比如带有反冲反馈的游戏鼠标。休息后的视频。

 [https://www.youtube.com/embed/Fs9OwsaYeDM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Fs9OwsaYeDM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

