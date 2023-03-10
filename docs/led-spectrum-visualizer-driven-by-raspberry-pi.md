# 树莓 Pi 驱动的 LED 光谱可视化仪

> 原文：<https://hackaday.com/2021/02/22/led-spectrum-visualizer-driven-by-raspberry-pi/>

早在 20 世纪 80 年代，音频设备上的频谱显示是绝对*必须的，*审美开始定义这个时代。这种风格一直延续到 20 世纪 90 年代，直到今天仍然很酷。[【Arduino Guy】决定用树莓派和大型 LED 显示屏组装这样一个显示屏。](https://www.hackster.io/gatoninja236/raspberry-pi-audio-spectrum-display-1791fa)

问题中的 LED 显示器是 64×64 RGB 类型，可从 Aliexpress 和其他电子供应商在线获得。为了运行显示，Adafruit RGB 矩阵帽与树莓 Pi 3B 一起使用，这使得驱动面板变得不在话下。视觉效果通过 Python 脚本运行，该脚本播放波形文件并通过快速傅立叶变换生成频谱图形。

虽然代码不能作为在 Raspberry Pi 上播放的任何内容的通用均衡器显示，但创建这样一个脚本对读者来说可能是一个有趣的练习。或者，可以将 Pi 连接到麦克风，根据室内环境噪声运行显示。在任何情况下，我们以前都见过类似的伟大项目，[比如这个基于激光的显示器](https://hackaday.com/2019/02/13/laser-light-show-turned-into-graphical-equalizer/)。休息后的视频。

 [https://www.youtube.com/embed/PAjNA0UocOs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PAjNA0UocOs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

