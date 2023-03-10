# 用坏苹果挑战 16×2 LCD 的极限！！

> 原文：<https://hackaday.com/2022/06/14/pushing-the-limits-of-a-16x2-lcd-with-bad-apple/>

虽然低对比度、蓝底略浅的 16 字符双线液晶显示器非常受欢迎，但它们确实是专门为字母数字用途制造的。它们在显示一些字符方面做得很好，但是它们并没有作为非字符用途的显示器出现在脑海中。但是[在 16×2 的 LCD 上显示视频是可能的](https://hackaday.io/project/185859-streaming-video-on-1602-character-lcd-display)，只要你愿意稍微扩展一下“视频”的定义，并在观看时发挥一些想象力。

正常情况下，16×2 显示器在每个点只能显示一个从固定字符集中选择的字符。但是[arduinocelantano]能够利用显示器允许的八个自定义字符槽从任意 5×8 像素位图构建图像。在使用`ffmpeg`将原始视频缩放到八个字符的视口后，使用 Python 程序将缩放后的视频的每一帧转换成代码，为视口的每个块生成自定义位图。即使显示器的刷新率较低，帧尺寸缩小，结果也是一个可识别的视频，毫无疑问，这得益于影子木偶*坏苹果的选择！！*视频。休息之后来看看效果如何。

不久前，我们在 LCD 上看到了相同视频的类似渲染；这种努力是惊人的，因为它是一个只有 EEPROM 的实现，以及更大的 LCD 和更好的对比度。那个项目是[arduinocelantano]在这里建造的灵感来源，在某些方面，我们认为它看起来更好一些——也许是反转的像素。不管怎样，向两位建设者脱帽致敬，他们突破了常规的限制，教给我们一些有趣的东西。

[https://player.vimeo.com/video/717239851](https://player.vimeo.com/video/717239851)

The [HackadayPrize2022](https://prize.supplyframe.com) is Sponsored by:[![Digi-Key](img/e7d13a315fd6226594212ca8f8762832.png)](https://www.digikey.com/)[![Supplyframe](img/fdb8a432506edeeafacfef227b3d3b33.png)](https://supplyframe.com/)