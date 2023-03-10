# Epic Clock 为 Unix 纪元计时

> 原文：<https://hackaday.com/2018/09/18/epic-clock-clocks-the-unix-epoch/>

承认吧:当你第一次听说 Unix 纪元的概念时，你坐下来用一个计算器计算从 1970 年 1 月 1 日午夜开始的 2 -1 秒是什么时候。就我个人而言，大约在我的公司雇用承包商在每一件看起来可能装有计算机的设备上贴上“Y2K 嫌疑人”标签的时候，我做了这个计算，所以这个大日子将在 2038 年的某个时候到来的事实既令人欣慰又令人害怕。

[叉车]同样被 Unix 纪元的想法迷住了，并且[建造了一个时钟来显示它](https://hackaday.io/project/161257-gpsclock)，至少在接下来的 20 年左右。为了适应最终的最大值 2，147，483，647，以及更实用的 ISO-8601 格式，需要比通常的时钟多几个数字，确切地说是 16 个。蓝色的七段显示器在光滑的木箱中留下了深刻的印象，遗憾的是在建造日志中没有关于它的细节。但内部是有据可查的，包括一个 GPS 模块和一个 RTC。时钟解析来自卫星的 NMEA 时间字符串，并同步 RTC。下面有一个简短的视频，展示了时钟的运行情况。

我们真的很喜欢[叉车]的时钟的外观，看着秒计数到最终溢出似乎是度过未来二十年的一种有趣的方式。当然，这不是我们推出的第一个纪元时钟，但它非常漂亮。

[https://videopress.com/embed/cbhcZqCS?hd=1&cover=1&loop=0&autoPlay=0&permalink=1&muted=0&controls=1&playsinline=0&useAverageColor=0](https://videopress.com/embed/cbhcZqCS?hd=1&cover=1&loop=0&autoPlay=0&permalink=1&muted=0&controls=1&playsinline=0&useAverageColor=0)