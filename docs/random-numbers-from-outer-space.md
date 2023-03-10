# 来自外太空的随机数

> 原文：<https://hackaday.com/2020/01/20/random-numbers-from-outer-space/>

需要随机数吗？当然，你可以掷骰子，但如果你这样做，你可能会引来附近量子爱好者的笑声。如果你真正需要的是不可预测的随机数，那就看看背景辐射吧，它会从安全的天体藏身处不断轰击我们。

[![](img/729a9bdc97905893fbb18e90935f60c0.png)](https://hackaday.com/wp-content/uploads/2020/01/visit-the-anode.png) 【阿尔法凤凰】[打破了数码管制造时钟的常规，设计了一个μ介子驱动的随机数发生器](https://www.youtube.com/watch?v=gwIGnATzBTg)，围绕着那温暖的复古光芒。μ子是亚原子粒子，类似于电子，但更重，是在介子进入大气层并经历放射性衰变时产生的。盖革-米勒管是全世界盖革计数器的支柱，它检测这些进入的μ子，并用它们来产生数字。

在盒子里，处于非稳态模式的 555 驱动一个十进制计数器，它通过结实的晶体管在谢妮上顺序输出数字 0-9。当 G-M 管等待μ介子时，这些数字只是重复循环，看起来很漂亮。当一个μ介子击中电子管时，第二个 555 会告诉十进制计数器立即停止。宾果，你有你的随机数！这种方法唯一的问题是，如果你马上需要一个数字，你可能不得不去拿一个香蕉，在 G-M 管附近挥舞它。

不管这一切是否有意义，你应该看看[Alpha-Phoenix]的项目视频，它既有趣又有启发性。他正在计划一个后续视频，重点是 G-M 管的随机性，所以请留意。

寻找一种更便宜的方法来捕捉你的随机数？你可以用一个鱼缸、一些气泵和一点 OpenCV 来完成。

 [https://www.youtube.com/embed/gwIGnATzBTg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gwIGnATzBTg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



通过[遥控/电子](https://www.reddit.com/r/electronics/comments/eluq11/i_just_finished_up_an_alldiscrete_quantumrandom/)