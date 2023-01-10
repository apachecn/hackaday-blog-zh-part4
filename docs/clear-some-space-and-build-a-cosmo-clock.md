# 清理一些空间，建立一个宇宙钟

> 原文：<https://hackaday.com/2020/05/10/clear-some-space-and-build-a-cosmo-clock/>

像我们许多人一样，[Artistikk]的灵感来自宇航员和太空旅行。为了保持灵感，他制作了 Cosmo 时钟——一个光滑的小时钟，每当宇航员被送入太空时，它就会改变颜色。

虽然太空很棒，但我们被这个项目中节约地球资源的重复利用所鼓舞。真正的报时来自回收的手表机芯。[Artistikk]从一个塑料容器中为它切下一组更大的指针，并用另一个容器的盖子作为钟的主体。

发射查询由 ESP8266 处理，它使用一个 Blynk 应用程序和一些 IFTTT 魔法，每当美国宇航局将宇航员送入太空时都会收到通知。然后，ESP 生成随机的 RGB 值，并将它们发送到单个 RGB LED。钟体足够小，单个 LED 的亮度足以照亮所有没有被厚纸涂黑的部分。如果你想知道，边缘周围的图案不是随机的，这是“天空”的莫尔斯电码，但你可能已经知道了，对不对？冲过休息时间开始参观。

在太空中上发条的时钟要复杂得多。看看这张从 90 年代末的联盟号宇宙飞船上拆下来的时钟。

 [https://www.youtube.com/embed/pxX_NdIVgNU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pxX_NdIVgNU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

