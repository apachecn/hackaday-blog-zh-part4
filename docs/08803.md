# 构建一个 8 位 CPU 来知道“但是它是怎么知道的？”

> 原文：<https://hackaday.com/2021/01/02/build-an-8-bit-cpu-to-know-but-how-do-it-know/>

大约在 2009 年的某个时候，[J. Clark Scott]出版了一本书，旨在通过从头开始构建 8 位 CPU 来为每个人揭开计算机的神秘面纱。这本书有一个吸引人但有点令人困惑的标题*但是它是怎么知道的呢？*。书名的背景故事是这样的:乔是个很好的人，但总是有点迟钝。他走进一家商店，一名售货员站在一群人面前的肥皂箱上。推销员正在推销奇迹般的新发明——热水瓶。他说，“它让热的食物保持热，让冷的食物保持冷……”乔对此思考了一分钟，对这项新发明感到惊讶，这项新发明能够根据你放入的食物种类来决定它应该做两件不同的事情中的哪一件。他无法抑制他的好奇心，他跳上跳下，在空中挥舞着他的手臂，说“但是，但是，但是，但是……”最后他冲口而出，他的燃眉之急，“但是它是怎么知道的？”乔看了看这个热水瓶能做什么，决定它一定能感应到它里面的东西，然后相应地执行加热或冷却操作。乔关于瓶子如何工作的概念远比事实复杂。在这个介绍性的开头，[J. Clark Scott]继续讲述基础数论，介绍逻辑门，最后是 8 位 CPU。

[Patrick LeBoutillier]决定建造[一个硬件版本的 CPU/计算机](https://hackaday.io/project/176526)，如[约翰·克拉克·斯科特]书中所述。为了将尺寸和成本控制在合理的范围内，他选择了微控制器和 SN74HC 逻辑 ic 相结合的混合结构。当作为阅读这本书的配套项目时，他希望人们可以亲自动手尝试一下。他已经发布了一系列 14 个视频，涵盖了 CPU 的构造，第一个介绍性视频在下面的休息后嵌入。对于该项目的微控制器部分，他使用四个 Arduino Nanos，代码和安装说明可在他的 [Git repo](https://github.com/patrickleboutillier/jcscpu-hmc) 获得。Fritzing 原理图，也可在回购，可能看起来有点令人生畏，但当你跟随他的视频系列，它变得容易。你可以在[预览这本书的前三章，“但它是怎么知道的？”](http://buthowdoitknow.com/preview.html)网站。

如果 FPGA 对你来说更重要，或者你想尝试学习 FPGA，那么[Patrick]有另外一系列 17 个视频(嵌入在下面)，他使用 [Digilent BASYS3 FPGA 开发板](https://reference.digilentinc.com/reference/programmable-logic/basys-3/start)完成相同的过程。这些并不是你唯一的选择——如果你只是想了解它是如何工作的，而不需要构建硬件，那么就去看看[Clark Scott] CPU 的[在线、基于浏览器的实现](http://buthowdoitknow.com/but_how_do_it_know_cpu_model.html)。

如果这种 8 位 CPU 的试验板看起来很复杂，那么这种国产的 8 位 CPU 是一种结实的 Blinky Build 和一个名副其实的跳线老鼠窝。

 [https://www.youtube.com/embed?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLYE0XunAbwfDvfabOlNWLViRcMI54M6CR](https://www.youtube.com/embed?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLYE0XunAbwfDvfabOlNWLViRcMI54M6CR)



 [https://www.youtube.com/embed?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLYE0XunAbwfBt2wXgDHEYPtILpimne_R9](https://www.youtube.com/embed?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent&listType=playlist&list=PLYE0XunAbwfBt2wXgDHEYPtILpimne_R9)

