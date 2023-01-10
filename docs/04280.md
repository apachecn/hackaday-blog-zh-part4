# 多亏了 Arduinos 和 DMX，智能地图上演了一出好戏

> 原文：<https://hackaday.com/2019/09/24/smart-map-puts-on-a-show-thanks-to-arduinos-and-dmx/>

当您正在处理的数据影响到一个国家的人口规模时，地图是传达信息的一种很好的方式。[jwolin]为一家非营利组织工作，希望找到一种方法来帮助人们直观地了解他们的业务范围和他们处理的原因。为了做到这一点，他创造了一个漂亮的智能地图墙显示器。

展示由一张世界地图组成，由中密度纤维板切割而成，贴在砖墙上。该系统还包括两个 4K 三星显示器。顶部的监视器显示标题，以使数据符合上下文，而底部的屏幕显示相关的全动态视频。一系列由 DMX 控制的灯光以各种不同的配置在世界地图上闪耀，以突出感兴趣的区域。

这个系统需要微妙的协调才能干净利落地运转。系统中有三台 Windows 10 电脑，每台显示器一台，世界地图一台。自动热键脚本在第一台计算机上运行，它选择一个随机视频，然后通过串行向 Arduino Nano 发出命令。这个 Arduino nano 然后与另外两个进行通信，确保第二个屏幕和 DMX 照明设备随后播放正确的匹配序列，与主视频保持同步。特别注意确保过渡尽可能平滑，每个序列之间没有间隙。整个安装很容易更新，只需将额外的内容上传到 Dropbox 文件夹中，这对项目的未来发展至关重要。

这是一个引人注目的系统，有助于教育参观者该组织的使命。我们已经看到了其他创新的世界地图显示，[像这个时钟突出了世界各地的白天和黑夜](https://hackaday.com/2011/09/12/world-clock-simulates-night-and-day/)。休息后的视频。

 [https://www.youtube.com/embed/f5Fjqk-rGuk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/f5Fjqk-rGuk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

