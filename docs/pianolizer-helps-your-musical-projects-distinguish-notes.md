# Pianolizer 帮助您的音乐项目区分音符

> 原文：<https://hackaday.com/2022/04/26/pianolizer-helps-your-musical-projects-distinguish-notes/>

[斯坦尼斯劳·普塞普]给了我们一个 Pianolizer 项目——一个易于使用的音乐探索和可视化工具包，一个帮助你将声音转化为钢琴音符的音频频谱分析仪。你可以在各种不同的设备上运行他的工具包，从 Raspberry Pi 和 PC 到任何配备浏览器的设备，包括智能手机，并按照你的意愿使用它的笔记输出。为了展示他的工具包，他在 Raspberry Pi 上安装了它，Python 代码获取音符数据并将颜色信息发送到 LED 条，[在 MIDI 键盘上演奏音符时实时显示音符！](https://youtube.com/watch?v=UVvdstcv4IY)他还创造了[浏览器版本](https://sysd.org/pianolizer/)，你可以使用麦克风输入或你选择的音频文件，所以你只需要打开一个网页来玩这个工具包的功能。

他花时间确保你可以在这个工具包的帮助下构建你的项目，为[提供使用说明](https://github.com/creaktive/pianolizer/blob/master/README.md#using-the-library=)和[命令行](https://github.com/creaktive/pianolizer/blob/master/README.md#using-the-cli-utility=)以及 [Python 示例](https://github.com/creaktive/pianolizer/tree/master/misc)，甚至分享了制作演示视频时使用的所有代码。感谢他分享的一切，现在您可以将钢琴音符识别添加到您的任何项目中！Pianolizer 是用 [JavaScript](https://github.com/creaktive/pianolizer/tree/master/js) 和 [C++](https://github.com/creaktive/pianolizer/tree/master/cpp/) (反过来编译成 WebAssembly)实现的自包含库，示例展示了如何在 Python 或其他语言中使用它。

[斯坦尼斯劳]还记录了代码背后的原理，用简单的术语解释了笔记识别是如何发挥其魔力的，但也给出了许多见解。我们习惯于将快速傅立叶变换(FFT)作为频谱分析的首选方法，也就是识别数据流中的不同频率。然而，通用 FFT 算法并不适合音符，因为音符频率之间的间隔会随着频率的增加而变宽，您需要做更多的工作来区分音符。在这个工具包中，他使用了滑动离散傅立叶变换(SDFT)算法，并向我们解释了他如何从音符频率中推导出参数。在文档的最后，如果你想进一步探讨这个话题，他还会给你[很多有用的参考资料](https://github.com/creaktive/pianolizer/blob/master/README.md#influenced--inspired-by=)！

你打算用这个造什么？也许，一个录下你吹笛子的盒子[瞬间变成活页乐谱](https://hackaday.com/2019/12/29/turning-sounds-from-a-flute-into-sheet-music/)？或者，当你停下来的时候，[会为你继续唱这首歌。](https://hackaday.com/2017/09/06/raspberry-pi-ai-plays-piano/)

 [https://www.youtube.com/embed/UVvdstcv4IY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UVvdstcv4IY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

