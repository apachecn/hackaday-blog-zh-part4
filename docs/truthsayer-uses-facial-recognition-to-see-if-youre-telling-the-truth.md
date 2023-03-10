# Truthsayer 使用面部识别来判断你是否在说真话

> 原文：<https://hackaday.com/2022/09/02/truthsayer-uses-facial-recognition-to-see-if-youre-telling-the-truth/>

观看[马克·扎克伯格]2018 年的国会证词，很难不得出这样的结论:他至少与普通人有很大不同。当然，建立了一家数十亿美元的公司，彻底改变了人们沟通方式的一切，这是非常确凿的证据，但这些镜头至少为这种人工智能真理检测算法提供了一个有趣的测试案例。

现在，我们并不是说这些视频中的任何人都在撒谎，弗莱彻·海斯勒也不是。他的算法分析了一个人的视频，并使用机器视觉来提取可能与不诚实压力有关的线索，这一算法远非完美。但正如下面的第一个视频所示，在工作中看到它非常有趣。这个想法是捕捉数据，如脉搏率，凝视方向，眨眼率，嘴部姿势，甚至手的位置，并用它们作为说谎的代理。第二个视频，来自【弗莱彻】最近的 DEFCON 演讲，有更多的细节。

这一切的关键是使用 OpenCV 和 MediaPipe 的人脸网格在视频中找到人脸——当[扎克]在镜头前时，这项任务似乎经常失败。通过观察血液流经受试者脸颊时颜色的细微变化来检测受试者的脉搏，我们已经听说过很多次了，但从未见过如此清晰地呈现和如此简单地执行。注视方向、眨眼和嘴唇收缩也很容易察觉。[Fletcher]还加入了 FER 图书馆进行面部表情识别，以了解受试者的情绪。总的来说，这些线索形成了对受试者真实性的粗略估计，[弗莱彻]很快指出这只是为了娱乐目的，完全不应该在下一次 Zoom 通话中用于你的同事。

【弗莱彻】的面部网格看起来眼熟吗？应该是，因为我们曾经看着他在一次编码面试中扭来扭去。

 [https://www.youtube.com/embed/5q-BQ2Q_pqI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5q-BQ2Q_pqI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/6esc_HD7b-A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6esc_HD7b-A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

