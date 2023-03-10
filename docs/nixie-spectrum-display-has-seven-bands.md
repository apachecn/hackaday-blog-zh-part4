# 谢妮频谱显示有七个波段

> 原文：<https://hackaday.com/2022/04/13/nixie-spectrum-display-has-seven-bands/>

光谱可视化仪总是一个有趣的项目，但我们真的很喜欢[Yannick99]的这个项目，因为它使用了[7 个 13 英寸谢妮管来显示](https://www.instructables.com/Audio-Spectrum-Visualizer-IN-13-7-Band/)。当然，电子管需要高电压，所以项目的一部分是高压电源。使用运算放大器和 MSGEQ7 滤波器 IC 时，频谱部分更普通一些。

芯片给微控制器供电，微控制器在一点帮助下驱动电子管。结果很棒，你可以在下面的视频中看到。还有其他几个视频展示了测试和原型制作。MSGEQ7 是一款可爱的芯片，可以从微控制器中卸载常见的 FFT 逻辑。它完成所有的工作，并以一种非常不寻常的方式进行交流。你重置设备，然后脉冲选通输入。这导致对应于 63 Hz 频带电平的模拟电压出现在输出引脚上。另一个选通脉冲选择下一个波段，你只是无限重复，这是微控制器擅长的。

唯一的问题，当然，是定位在-13 管。如果你寻找它们，它们就在你身边，但它们可能并不便宜。预计为他们每人支付大约 20 美元，或多或少。我们想知道你是否能[制造一个看起来像 LED 的替代品](https://hackaday.com/2022/04/05/led-filaments-make-a-retro-clock-without-any-retro-parts/)。如果你想知道这些管子的寿命，有人的[已经做了测试](https://hackaday.com/2013/11/24/measuring-the-lifespan-of-nixie-tubes/)。

 [https://www.youtube.com/embed/lLZEa1IzzaU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lLZEa1IzzaU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

