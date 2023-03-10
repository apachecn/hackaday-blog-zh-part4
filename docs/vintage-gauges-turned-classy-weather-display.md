# 老式仪表变成了经典的天气显示

> 原文：<https://hackaday.com/2020/08/08/vintage-gauges-turned-classy-weather-display/>

看到旧硬件从垃圾堆中被拯救出来总是件好事，尤其是当最终结果像[Build Comics] 制作的这个[模拟天气显示器一样令人印象深刻的时候。它最终成为了一个真正的多学科项目，不仅结合了修复工作和现代微控制器技术，还加入了一些木工。](https://buildcomics.com/uncategorized/ts-temperature-humidity-meter/)

[![](img/613dd19cec87c6a155b51bf7fbba4c81.png)](https://hackaday.com/wp-content/uploads/2020/08/analogwx_detail2.jpg) 自然，仪表本身才是节目的真正明星。他们开始时有生锈的内部零件和破碎的玻璃，但来自一位牺牲者的零件和来自[Build Comics]的一些 TLC 让他们恢复了正常工作。我们特别喜欢让刻度标记看起来真实的努力，GIMP 中修改了原件的扫描，以指示温度和湿度，同时保留了相应的时期细节。

为了驱动 20 世纪 40 年代的指示器，[Build Comics]使用了 Arduino Nano 和 DHT22 传感器，可以检测温度和湿度。包括几个微调罐，用于微调压力表，所有东西都安装在定制松木外壳内隐藏的一小块 perfboard 上。

这不是我们第一次看到模拟仪表被连接到现代电子设备上，但是大多数 T2 项目只是现代的 T3。虽然最终的外观可能有些两极分化，但我们认为[保持硬件的经典风格](https://hackaday.com/2016/01/27/old-school-gauges-let-you-know-which-way-the-wind-blows/)是正确的选择。