# 步进控制锯自动完成一项繁琐的工作

> 原文：<https://hackaday.com/2019/08/10/stepper-controlled-chop-saw-automates-a-tedious-job/>

我们不会质疑为什么[光的吸收器]需要切割大量的铝原料碎片。我们假设他的推理是合理的，所以我们感兴趣的是[他建造的自动化锯](https://www.youtube.com/watch?v=bl16CQJarpQ)以使工作不那么单调乏味，并且可能不那么手指粗糙。

大概有很多方法可以完成这项工作，但是[吸收器]没有留下什么线索来解释他为什么选择这个特殊的设置。不管是什么原因，这个构建看起来很有趣，一个长的步进驱动螺纹杆推动一个追随者沿着轨道到一个标准的锯子。铝原料骑在轨道上，被推出一个设定的数量，然后被切断干净，因为运行锯是由一个线性驱动器降低。然后，循环重复，直到股票没有了。

Arduino 以通常的方式控制 stock-advance 步进器，但线性致动器的控制方法有些非常规。第二个步进电机在轴上有两个偏移 180°的凸轮。凸轮驱动四个微型开关，这些开关以 H 桥结构设置。步进器前后旋转，首先在一个方向上运行线性致动器，然后在另一个方向上运行，中间有一个中间位置。这是一种有趣的方法，使用机械隔离而不是典型的光学隔离。看看下面的视频。

我们承认对这个装置产生的优惠券的用途有些好奇，所以也许我们会在评论区从[光的吸收器]那里得到一些细节。毕竟，我们确切地知道被类似的[“Auto Mega Cut-O-Matic”](https://hackaday.com/2019/06/29/automatic-cut-off-saw-takes-the-tedium-out-of-a-twenty-minute-job/)切割的铜管的用途。

 [https://www.youtube.com/embed/bl16CQJarpQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bl16CQJarpQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

