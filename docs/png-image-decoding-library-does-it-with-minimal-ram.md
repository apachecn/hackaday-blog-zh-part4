# PNG 图像解码库用最少的内存来完成

> 原文：<https://hackaday.com/2021/07/17/png-image-decoding-library-does-it-with-minimal-ram/>

想要在连接到 Arduino 或其他微控制器板的显示器上显示 PNG 文件吗？你会想看看[Larry Bank]的 [PNGdec，Arduino 友好的 PNG 解码器库](https://bitbanksoftware.blogspot.com/2021/05/an-embedded-friendly-png-decoder.html)，它使得在你选择的微控制器上处理 PNG 文件更加容易。

PNG 图像格式支持无损压缩等有用的功能，通常是作为 GIF 文件的一种改进(非专利)替代方案而开发的。到目前为止，一切都很好，但事实证明，在微控制器上解码 PNG 文件是一个挑战，因为与台式机相比，内存量有限。当 PNG 规范在 90 年代开发时，计算机很容易拥有兆字节的内存，但微控制器往往以千字节为单位来衡量内存，缺乏高级内存管理。[拉里]的图书馆解决了这些问题。

PNGdec 是自包含的，没有外部依赖性，并且还具有一些功能，可以轻松地为不同的显示类型转换像素格式。它可以在任何至少有 48 K 内存的微控制器上运行，所以如果这听起来有用，那么[查看 GitHub 仓库中的代码和示例](https://github.com/bitbank2/PNGdec)。

我们之前已经看到了[Larry]在[优化 GIF 播放](https://hackaday.com/2020/08/03/optimizing-gif-playback-for-microcontrollers/)以及[快速 JPEG 解码](https://hackaday.com/2020/08/26/new-arduino-jpeg-library-focuses-on-speed/)方面的出色工作，随着爱好者继续看到小型 LCD 和基于有机发光二极管的显示器变得越来越容易获得和负担得起，这些库的相关性越来越大。

*【巴新 logo: [巴新首页](http://www.libpng.org/pub/png/)*