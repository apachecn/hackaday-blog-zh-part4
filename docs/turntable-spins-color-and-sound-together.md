# 转盘将颜色和声音一起旋转

> 原文：<https://hackaday.com/2019/10/27/turntable-spins-color-and-sound-together/>

如果你不能培养自己的联觉，买电子产品来帮你也没关系。这就是艺术家 Xavier Gazon 创作的半音阶的情况，他将各种电子产品变成弯曲的音乐艺术品。他的项目将一个旧的飞利浦音乐 5120 转盘变成了一个彩色的 MIDI 音序器，其灵感来自于 20 世纪的旧乐器，如 Optophonic 钢琴和 Luminaphone。

半音阶使用放置在转换转盘上的彩色圆盘来执行给定音阶的和弦循环序列，生成 MIDI 数据作为输出。它的灵感使用原始光学作为他们的媒介，这个项目使用一个微小的微控制器和两个现代光学传感器来完成这项工作。其中之一是一个简单的红外传感器，它跟踪转盘边缘的白点，产生 MIDI 时钟信号，以保持一切量化和同步。另一个是安装在音臂上的颜色传感器，可以分辨出看到的是什么颜色，以及音臂离转盘的高度。

虽然该仪器仍处于测试阶段，但如何产生音符的细节尚未给出，尽管总体想法是，它们是由拾音器臂看到的颜色及其在盘子上方的位置决定的。移动拾音器臂可以改变它跟踪的 pucks，转盘的速度也可以调整，从而改变旋律的声音。​

CHROMATIC 是一个非常有趣的项目，但它不是我们在这里看到的第一个基于光学的转盘黑客。我们也看到了[对颜色传感器](https://hackaday.com/2018/07/08/rgb-sensors-new-job-cryptocurrency-trade-advisor/)更奇怪的用法。休息过后，请看这段视频。

 [https://www.youtube.com/embed/ljxQYGn5PMU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ljxQYGn5PMU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

