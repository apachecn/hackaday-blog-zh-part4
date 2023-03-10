# 字符 VFD 成为频谱分析仪

> 原文：<https://hackaday.com/2022/05/24/character-vfd-becomes-spectrum-analyzer/>

如今，流媒体服务是在电脑上或在旅途中欣赏音乐或播客的绝佳方式。然而，它们缺少 MP3 播放器和老式带子的一个特征:可视化！[mircemk]是这些的粉丝，他已经建造了一个硬件频谱分析仪，可以随着音乐一起泵送。

该建筑依靠 20×2 字符的 VFD 显示器，它看起来很棒，具有高亮度和出色的对比度。它可以轻松地由微控制器驱动，因为它有一个与典型 HD44780 命令集兼容的片上控制器。在 Arduino 平台上，这意味着显示器可以通过流行的 LiquidCrystal 库轻松驱动。

Arduino Nano 内部通过模拟输入接收音频信号。然后，它使用 fix_fft 库处理音频，该库运行快速傅立叶变换，以计算出左右声道音频频谱中每个频率仓的能量水平。然后，这些数据被发送到屏幕上进行显示。它令人印象深刻的快速和流畅，随着[mircemk]用一些曲调测试它，显示器随着节拍跳舞很好。

如果它看起来很熟悉，那是因为它是[mircemk]以前项目的更新版本。我们之前把它看作是一个随着节拍跳动的 VU 计[，](https://hackaday.com/2022/03/09/vfd-character-display-turned-into-audio-vu-meter/)一个更简单的可视化，但仍然很酷。休息后的视频。

 [https://www.youtube.com/embed/MmLOjRUFaSg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MmLOjRUFaSg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

