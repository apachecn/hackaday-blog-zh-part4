# 联网的夜灯一起发光

> 原文：<https://hackaday.com/2021/03/13/networked-nightlights-glow-together/>

夜灯是让怕黑的孩子安静下来的好方法，也能避免你的脚趾碰到走廊里的家具。然而，在这个万物互联的时代，他们可以做得更多。[Andy]想出了一个很好的方法来做到这一点，[创建一个高级的网络解决方案来满足他的需求。](https://www.hackster.io/andy-warburton/networked-nightlights-with-esp8266-and-raspberry-pi-4c5a56)

[Andy 的]小夜灯不仅能以通常的方式使用，还能为他的孩子提供指示。根据一天中的不同时间，颜色会发生变化，这表明是该睡觉了，还是早上起床开始看卡通片太早了。房子周围的每个小夜灯都由一个 ESP8266 运行，它使用一组 WS2812B LEDs 照明。ESP8266 根据运行在 Raspberry Pi 上的基本 web 服务器的命令决定颜色值，每分钟更新一次。这给了[Andy]在一个地方做出改变的灵活性，然后自动在整个 Nightlight Network (TM)上铺开。

这是一种有趣的方式，教孩子们不要破坏一个美好的周六睡眠，也可以作为一个有趣的彩色小夜灯。当然，豪华智能夜灯正在成为一种事物，正如这个蓝牙设备的拆卸所显示的。如果你已经建立了自己的网站，[一定要给我们写信！](http://hackaday.com/submit-a-tip)