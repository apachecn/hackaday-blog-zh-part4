# 迷你湿度计包电子纸显示器

> 原文：<https://hackaday.com/2021/03/16/mini-hygrometer-packs-e-paper-display/>

从历史上看，显示技术一直是耗电大户。过去，阴极射线管和白炽灯泡像喝免费啤酒一样吸收电子。最终，led 和 LCD 的出现大大降低了功耗，但低功耗显示技术之王仍然是 ePaper 和 eInk 显示器。只有在刷新显示器时才需要电源，它们可以无限期关闭，消耗很少甚至没有电流。这对于低功耗产品来说非常好，比如安德鲁·拉姆琴科的微型湿度计。(视频，嵌在下面。)

该版本运行在 nRF52811 微控制器上，连接到 1.02 英寸的电子平板显示器上，价格仅为 7 美元。然后查询 SHT20 温度和湿度传感器，对环境条件进行采样，并将结果显示在屏幕上。这样做的好处是，该设备可以由硬币电池供电，并设置为不定期更新——比如每小时一次。然后，用户可以检查它，而不必打开。

低功耗设计意味着它将是一个完美的设备，可以一次放在吉他盒或保湿盒里几个月。另外，由于板载蓝牙功能，它还能够集成智能家居。将它升级成一个鸣叫的雪茄盒可能是微不足道的，[自 2009 年](https://hackaday.com/2009/09/21/tweetidor-the-tweeting-humidor/)以来我们就没有见过这样的雪茄盒！

 [https://www.youtube.com/embed/2zTEHTAr7lk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2zTEHTAr7lk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

