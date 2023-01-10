# 数字雨动画挤进 Pi Pico

> 原文：<https://hackaday.com/2022/01/12/digital-rain-animation-crammed-into-pi-pico/>

随着一部新的 *Matrix* 电影在电影院上映，我们都想起了那些屏保，它们是 1999 年第一部电影上映时*最酷的东西*。【en0b】决定[在树莓派 Pico](https://github.com/en0b/pico-display-matrix) 上重现经典的“数字雨”效果，在这个过程中用尽了所有小微控制器的存储。

与其依赖现有的图形库，[en0b]不如着手为动画使用高质量的 GIF。原始文件是 8 MB，这对于 Pico 来说太大了。然而，在图像编辑器中进行了一些欺骗之后，在定制 Python 脚本的帮助下，[en0b]设法将 127 帧的动画以 240 x 135 的分辨率放入芯片上的 2 MB 闪存中。微控制器连接到 Pimoroni 的 1.14 英寸 IPS“Pico Display”，最终看起来很棒，忠实地再现了电影中的美感。

[en0b]的技术可以可靠地用于显示任何 GIF，你可以把它削减到 14 到 16 色，而不会损失太多的质量。它不是世界上最高端的图形格式，但它可以处理像这样的小动画。

我们以前也见过类似的构建，使用更多重型硬件以几乎相同的方式构建[一个神奇的 8 球](https://hackaday.com/2021/05/06/shake-up-your-magic-8-ball-with-gifs/)。与此同时，如果你有自己的整洁的 GIF 小黑客或 Pico 项目，不要犹豫[发送它们！](http://hackaday.com/submit-a-tip)