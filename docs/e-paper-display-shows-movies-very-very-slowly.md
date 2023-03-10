# 电子纸显示器播放电影非常非常慢

> 原文：<https://hackaday.com/2020/08/23/e-paper-display-shows-movies-very-very-slowly/>

你有多喜欢一部耗时数月才完成的电影？我们认为这在很大程度上取决于电影；目前这一批来自《星球大战》系列的电影已经够长了，非常感谢。但是像《T2》或《T4 2001:太空漫游》这样的电影在这台超慢动作电子纸电影播放器上播放可能会是一种非常不同的体验。

自从[汤姆·惠特韦尔]看到[布莱恩·博耶]的概念以来，将一部电影的单帧显示几个小时而不是几毫秒的想法就吸引了他。[Tom]使用的硬件是相似的:一个树莓派，一个带 64 GB 电影卡的 SD 卡帽子，以及一个 Waveshare 电子纸显示器，所有这些都可以很好地放在宜家的相框中。

[![](img/f82a3fc6ff0a528c5ce0e162ffae20e3.png)](https://hackaday.com/wp-content/uploads/2020/08/raspberry-pi-epaper-movie-player.jpg) 【汤姆】的软件有点不一样，虽然；Python 程序使用 FFmpeg 以可配置的速率从电影中提取和抖动帧，以定制比原始视频更多的观看体验。每两分钟放映一帧，然后跳过四帧，他花了两个多月的时间才看完*惊魂记*。他报告说淋浴的场景在一天半内就结束了——几乎和拍摄的时间一样长——而马里恩·克雷恩开车穿过沙漠的场景花了几个星期才完成。我们一直想知道为什么[希奇]在那场戏上花了这么多时间。

加载适当的电影，我们可以看到这是一个有趣的方式来真正研究一部好电影的结构和流程。这也是一个让你接触电子纸显示器的好方法，我们已经看到它出现在从[气象站](https://hackaday.com/2017/09/27/an-arduino-weather-station-with-an-e-ink-display/)到 [Linux 终端](https://hackaday.com/2018/08/14/run-a-linux-terminal-on-cheap-e-ink-displays/)的所有地方。