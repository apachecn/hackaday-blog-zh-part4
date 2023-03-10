# 螺旋音乐可视化

> 原文：<https://hackaday.com/2021/11/26/spiral-music-visualization/>

在演奏时实时显示音符是一个非常强大的学习工具，但它通常用于学习如何演奏特定的乐器。这个话题实际上是一个学习音乐理论的好方法——音高如何共同作用来产生我们听到的声音。选择的视觉钉[将 12 个音符中的每一个排列成一个螺旋](https://tinkerings.org/2021/11/20/spiral-music-visualization-using-teensy-or-python/)。当你继续在音阶上上升更多的八度音阶时，同名的音高会排成一条线，就像从太阳投射出来的光线。因此音阶中的音符有 12 个音:c、C#/D♭、d、D#/E♭,F 等。

[mechatronicsguy]几年前建造了它，但现在才开始记录它，我们很高兴他这样做了。笔记的布局起初看起来就像一个丰富多彩的可视化。但是正如他在描述中提到的，这给每一种不同类型的绳索分配了一种形状。无论是用 c、G#、B♭还是任何其他音符作为根音弹奏，大和弦都具有相同的形状。该形状只是基于该根音符绕轴旋转。较高的八度音阶将在半径上显示得更远，但和弦形状仍将保持不变。小和弦、增强和弦、偶数和弦以及增加音高的和弦在显示屏上都有自己独特的形状。

通过观看下面视频中的 Python 渲染版本，您可以获得对可视化的最佳理解。这是一个很好的接触，音符在释放后变成灰色并逐渐消失，所以你可以看到当前和弦的来源。严格来说，这不是预先录制的额外津贴。虽然你可以给它提供 MIDI 文件，但你也可以演奏 MIDI 乐器，并在使用带音频屏蔽的 Teensy 的硬件版本上实时显示视觉效果。

如果你在寻找如何使用音乐可视化工具来教授乐器的例子，只需看看这个 Wurlitzer 音符可视化工具的复制品。另外，对于那些不知道的人来说，硬件演示(下面的第二个视频)中正在播放的歌曲是贝多芬的第七交响曲。[值得一听的](https://www.youtube.com/watch?v=-4788Tmz9Zo)，它会改变你的生活。

 [https://www.youtube.com/embed/H3ucHiadx2w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/H3ucHiadx2w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/7xVirr0APKk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7xVirr0APKk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

