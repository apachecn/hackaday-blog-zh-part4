# 构建镶嵌新像素时钟

> 原文：<https://hackaday.com/2022/10/01/building-a-tessellated-neopixel-clock/>

任何人都可以买一个钟，但是自己动手制作可以让你在这个过程中展示你的创造力。[爱迪生科学角]通过这个简洁的科幻外观设计做到了这一点。

该版本依靠 Arduino Pro Mini 来运行该节目，并与 DS3231 实时时钟模块配对。后一部分非常重要，因为没有它，Arduino 就不能保持准确的时间。3D 打印的外壳从外面看起来毫无特色。然而，在内部，它有一个整洁的三角形结构，允许时间以吸引人的三角形方式显示。在所有的片段之间有一个黑色的塑料隔板，可以阻止不美观的渗色，真正有助于最终效果。每个三角形都由一个新像素 LED 点亮，这两个 LED 都是可寻址的，并且能够以 RGB 颜色点亮。这是一个有吸引力的和丰富多彩的展示。

如果你想尝试一些更传统但更具挑战性的东西，[考虑制作自己的 7 段显示器](https://hackaday.com/2013/12/03/fabricate-your-own-7-segment-displays/)。休息后的视频。

 [https://www.youtube.com/embed/HbU2dGO_xr4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HbU2dGO_xr4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

