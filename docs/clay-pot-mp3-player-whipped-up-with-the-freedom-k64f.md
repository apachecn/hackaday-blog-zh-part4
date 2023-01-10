# 粘土罐 MP3 播放器与自由-K64F 搅在一起

> 原文：<https://hackaday.com/2021/04/24/clay-pot-mp3-player-whipped-up-with-the-freedom-k64f/>

在流媒体时代，我们中很少有人会每天都想着 MP3。我们的音乐收藏由来自遥远国度的流媒体公司的敌对高管管理。然而，对[vinod]来说，它们仍然是有用的——因为他刚刚给自己做了一个 MP3 播放器，可以放在一个陶罐里。

构建基于 FRDMK64F 开发板，封装了强大的 120 MHz ARM 芯片。这有足够的咕噜声来解码 MP3 的飞行，使用螺旋 MP3 解码器库。MP3 本身通过 SD 卡传输，使用更快的 SDIO 访问方法，而不是依赖更慢的 SPI。解码后，产生的 PCM 音频数据利用芯片的 DMA 硬件通过 DAC 输出，从而实现平滑、无毛刺的回放。输出到一个大低音扬声器是通过一个 15 W 的 D 类放大器，整个钻机从一个 USB 电源组供电。

用大量的热胶将所有的电子元件堆在一个大的低音扬声器的背面，最终的结果是非常壮观的；尤其是安装在一个陶罐里，作为低音反射音箱的时候。[在](https://hackaday.com/2019/05/17/yet-another-concrete-speaker-build/)之前，我们已经看到了一些混凝土铸造的扬声器，但远远没有足够的粘土黑客项目。请纠正这一点，[，并在完成后通知我们](http://hackaday.com/submit-a-tip)。提前感谢—休息后的视频！

 [https://www.youtube.com/embed/FszHky4EFdY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FszHky4EFdY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

