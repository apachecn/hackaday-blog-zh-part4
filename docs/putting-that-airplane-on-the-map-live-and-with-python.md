# 将飞机放到地图上——用 Python 直播

> 原文：<https://hackaday.com/2018/12/03/putting-that-airplane-on-the-map-live-and-with-python/>

人类对飞机的迷恋从未间断。无论你是带着相机在外面，真实地一瞥飞机，还是带着 RTL-SDR 加密狗坐在家里，从远处看着它们，跟踪它们都是一项有趣的消遣活动。当然，前提是你住的地方离机场很近，或者在一个空中交通足够繁忙的地区。如果没有，那么总有在线实时跟踪可以依靠，正如[geomatics]将向您展示的，[您可以用几行 Python 代码构建自己的实时航班跟踪系统](https://www.geodose.com/2018/11/create-simple-live-flight-tracking-python.html)。

正如 Python 通常的情况一样，许多功能都是通过外部模块实现并随时可用的，这让您可以专注于实际的应用程序，而不必太担心细节。类似地，如今可以从各种公开可访问的 API 中请求大量数据。如果你正在寻找一个足够简单的例子，以便用一个现实世界的应用程序进入这两个主题，[geomatics]的飞行跟踪器使用[cartopy](https://scitools.org.uk/cartopy/)使用公开的街道地图数据创建地图，并从[ADS-B Exchange](https://www.adsbexchange.com/)的公共 API 检索航班信息。

我们之前已经看到几次提到 ADS-B 交换，例如这个基于 ESP8266 的飞机观察者和它的继任者的[。如果你对你周围的空中交通更感兴趣，](https://hackaday.com/2017/01/07/tracking-planes-with-an-esp8266/)[可能是时候买个 DVB USB 加密狗了](https://hackaday.com/2015/02/12/why-you-should-care-about-software-defined-radio/)。