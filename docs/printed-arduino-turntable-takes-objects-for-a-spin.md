# 印刷的 Arduino 转盘带着物体旋转

> 原文：<https://hackaday.com/2019/11/12/printed-arduino-turntable-takes-objects-for-a-spin/>

你造好 3D 扫描仪了吗？有多种方法可以模拟这些曲线和平面，但最简单的方法可能是摄影测量法——这是一种将一堆照片拼接成 3D 模型的方法。如果你建造了一台像布莱恩·布罗肯那样几乎可以自动完成所有事情的扫描仪，你可能会考虑开始一项扫描打印的兼职工作。

[![](img/889f10bba4adb4b8824a1ffccd68b6de.png)](https://hackaday.com/wp-content/uploads/2019/11/servo-punch.png) 这个小机器将物体旋转 360 度，并触发与 iPhone 相连的蓝牙遥控器。在自动模式下，它可以拍摄 2-200 张照片。有一种电影拍摄模式，可以拍摄物体缓慢旋转的视频，这使得任何东西看起来都至少比原来可怕 35%。第三种模式提供转盘位置和速度的手动控制。

Arduino UNO 控制步进器，步进器通过 3D 就地印刷轴承组件移动转盘。这个项目比我们在夏天看的[Brian]的[手摇版本有了(巨大的)改进，尽管两者本身都是艺术作品。](https://hackaday.com/2019/07/24/printed-it-hand-cranked-photography-turntable/)

除了轴承，我们最喜欢的部分是拍照过程本身。[Brian]无法让 iPhone 很好地播放 HC-05 或-06 模块，所以他让 9g 伺服的喇叭在蓝牙遥控器上点击快门按钮。这个美丽的野兽是敞开的，所以启动打印机。你可以在休息后观看转盘的设计和建造过程。

想扫描一些非常小的东西吗？用电影机器制作电动显微镜。

 [https://www.youtube.com/embed/SAgiv4o8rxQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SAgiv4o8rxQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

