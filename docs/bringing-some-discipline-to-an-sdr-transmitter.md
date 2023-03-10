# 给 SDR 发送器带来一些规则

> 原文：<https://hackaday.com/2022/07/13/bringing-some-discipline-to-an-sdr-transmitter/>

软件定义无线电(SDR)技术的普及对射频爱好者来说是天赐良机。基于 SDR 的接收器和发射器已经变得如此便宜，以至于你现在可能已经在你的长凳上放了一两根棍子——事实上，我们可以从我们坐的地方看到三根。

但便宜是有代价的，通常表现为频率稳定性，这在某些应用中可能令人望而却步，尤其是业余无线电，频谱卫生是最重要的考虑因素。因此，我们很高兴地看到[技术头脑] [通过使用 GPS 训练的振荡器来解决 SDR 频率稳定性问题](https://www.youtube.com/watch?v=o2IeXpsOQig)。该设置使用 ADALM-PLUTO SDR 收发器和来自利奥博德纳尔电子公司的精密振荡器[。振荡器可以通过编程在很宽的频率范围内输出坚如磐石的 GPS 标准信号。Pluto 有一个寻找 40 MHz 的外部振荡器输入，正好在 GPSDO 的范围内。](https://www.leobodnar.com/shop/index.php?main_page=product_info&cPath=107&products_id=301&zenid=6fc11763545e79762cba492eb4e9f041)

设置非常简单，只需使用 SMA 至 UFL 跳线将振荡器的输出插入 SDR 的外部时钟输入，并调整 SDR 和振荡器的设置。当然，并非所有 SDR 都有外部时钟输入，因此您的里程数可能会有所不同。但是如果你的设备配备合适，这看起来是一个获得高频率的好方法——下面的视频显示了未经训练的 SDR 可以漂移多少。

像任何一个好的火腿一样，[技术头脑]正在尽自己的一份力量来保持信号的干净和准确。他的这种设置的主要用例将是工作 [QO-100](https://hackaday.com/2019/03/18/eshail-2-hams-get-their-first-geosynchronous-repeater/) ，业余无线电的第一个地球同步卫星中继器。我们不得不说，我们这些生活在地球上三分之二没有被这颗卫星覆盖的地方的火腿，非常渴望能有一只(或两只)我们自己的地球同步鸟像这样一起玩耍。

 [https://www.youtube.com/embed/o2IeXpsOQig?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/o2IeXpsOQig?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

