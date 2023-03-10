# 廉价太阳能灯的拆卸与分析

> 原文：<https://hackaday.com/2020/01/26/teardown-and-analysis-of-a-cheap-solar-lamp/>

如果你走在一元店的过道里，你会在世界范围内看到一个不变的东西，那就是中国的太阳能灯。你的美元让你得到一个塑料背后的白色 LED，安装在一个长钉上，插在地上，顶部有一个太阳能电池。它白天在阳光下充电，然后在夜幕降临时点亮 LED 几个小时。它们在花园里随处可见，毫无疑问，垃圾填埋场到处都是，因为它们不会持续很长时间。【乔瓦尼·贝尔纳多】有一个坏了，所以他[把它拆了，看看发生了什么，是什么让它滴答作响](https://www.settorezero.com/wordpress/teardown-lampada-solare-cinese-da-giardino/)(意大利语，[谷歌翻译链接](https://www.settorezero.com/wordpress/teardown-lampada-solare-cinese-da-giardino/))。

正如所料，罪魁祸首被证明是一个泄漏和腐蚀的 1.2 伏 NiMh 电池，用 AA 电池替换它使灯复活。但是这个故事有趣的部分来自于他拆卸和分析灯的组件。它以 YX8016 电池充电器和电源管理芯片为中心。该设备具有惊人的设计经济性，只有四个组件，包括太阳能电池和 LED。最后一个元件是一个小电感，它构成升压转换器的一部分，在电池电压下降时保持 LED 点亮。该芯片以 580kHz 的频率切换，产生 3.2 伏的电源。

如果这是你感兴趣的话题，别忘了看看我们不久前举办的[能量采集挑战赛](https://hackaday.com/2018/07/24/twenty-power-harvesting-projects-headed-to-the-hackaday-prize-finals/)。