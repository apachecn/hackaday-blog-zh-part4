# 树莓π零点上更快的傅立叶变换

> 原文：<https://hackaday.com/2021/09/22/even-faster-fourier-transforms-on-the-raspbery-pi-zero/>

通常在计算中，我们开始做一件事，我们很高兴我们正在做这件事。但后来我们意识到，如果我们能做得更快，那就更好了。[Ricardo de Azambuja]在使用 Raspberry Pi Zero 时就遇到了这种情况，他意识到有一些技术可以在平台上大幅加快快速傅立叶变换(FFT)的速度。就这样，他开始工作。

诀窍是使用 Raspberry Pi Zero 的 GPU 来处理 FFT，而不是 CPU 本身。这使得 Ricardo 的一维 FFT 速度提升了 7 倍，二维运算速度提升了 2 倍。

这个想法抄袭了我们多年前的作品，它提供了与第一个树莓派相似的速度。鉴于 Pi Zero 使用与原始 Raspberry Pi 相同的 SoC，但时钟速率更高，这非常有意义。然而，在这种情况下，[Ricardo]用 Python 而不是 C 实现了代码，以适应他的用例。

[Ricardo]将该代码与他的[枫糖浆 Pi 相机项目](https://hackaday.com/2021/06/30/smart-camera-based-on-google-coral/)一起使用，该项目将 Coral USB 机器学习加速器与 Pi 零和相机配对，以实现自动车牌识别或面罩检测等任务。好玩！