# 坏苹果！！通过 Arduino Mega

> 原文：<https://hackaday.com/2019/01/08/bad-apple-via-the-arduino-mega/>

Arduino Mega 是制造者的有用工具。一般来说，一旦一个人想出了闪烁的 led 需要比 Arduino Uno 更多的 IO 的计划，他就会毕业到 Mega 并孤注一掷。然而，这不是我们通常认为的视频工作的首选。[【夏羽】不敢苟同，给这个坏苹果编码！！Arduino Mega 2560 的演示。](https://rv6502.ca/post/2018/01/22/bad-duino-bad-apple-on-arduino/)

对于那些不熟悉的人来说，Arduino 上的视频实际上是一个已经解决的问题—[只需要一对电阻和一些漂亮的代码。](https://hackaday.com/2012/05/16/controlling-a-tv-with-a-microcontroller/)这个黑客真正的肉是视频存储本身。以前也有人做过，但通过 SD 卡或串行链路传输数据。[夏羽]决定把所有东西都存储在 Arduino 上，于是黑客攻击开始了。视频数据以每像素 1 比特的方式存储，因为这是一个简单的黑白视频[按照最初的灵感](https://www.youtube.com/watch?v=UkgK8eUdpAo)。LZ77 压缩用于在不需要太多 ram 的情况下压缩数据，RAM 是 Mega 上的有限资源。这只是视频，因为 Mega 可以处理 3 分 39 秒的视频存储，但未来的工作可能包括与第二个 Arduino 同步，以提供配乐。

这是一次展示[夏羽]在有限的平台上获得令人印象深刻的性能的能力的黑客攻击。我们以前见过这种情况，[他出色的星狐港对阿杜博伊](https://hackaday.com/2019/01/07/star-fox-comes-to-arduboy/)。休息后的视频。

 [https://www.youtube.com/embed/IWJmK5J8shY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IWJmK5J8shY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

